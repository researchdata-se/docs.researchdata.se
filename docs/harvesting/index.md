# Introduction

For Researchdata.se to be able to harvest dataset metadata from a data source such as a repository, a machine actionable way to access the metadata is needed.

To avoid a Researchdata.se-specific method, we recommend using established metadata standards like DataCite XML via [OAI-PMH](oai-pmh.md) and/or Schema.org JSON-LD one the landing page via [sitemap.xml](sitemap-xml.md).

## Harvesting flow 
Metadata from national research data repositories is harvested and made available to other data portals and search engines.  
The figure below illustrates the harvesting flow.


``` mermaid
graph
  %% =========================================================
  %% REPOSITORIES
  %% =========================================================

  repo1[(Repository 1)]
  repo1_oai[Repository 1 \n OAI-PMH endpoint]

  repo2[(Repository 2)]
  repo2_sitemap@{ shape: doc, label: "sitemap.xml"}
  repo2_jsonld@{ shape: documents, label: "Landing page \nJSON-LD"}

  repo3[(Repository 3)]
  repo4[(Repository 4)]


  %% =========================================================
  %% DATACITE
  %% =========================================================

  datacite[(DataCite)]

  datacite_oai[DataCite\nOAI-PMH endpoint]
  click datacite_oai "https://support.datacite.org/docs/datacite-oai-pmh" "DataCite OAI-PMH endpoint"

  datacite_api[DataCite API]
  click datacite_api "https://support.datacite.org/docs/api" "DataCite API"


  %% =========================================================
  %% RESEARCHDATA.SE — INGESTION AND CATALOGUE
  %% =========================================================

  rda_harvester@{ shape: procs, label: "researchdata.se \n harvester"}

  rda_index[(researchdata.se \n elasticsearch)]

  rda_catalogue[researchdata.se \n catalogue]
  click rda_catalogue "https://researchdata.se/" "researchdata.se catalogue"


  %% =========================================================
  %% RESEARCHDATA.SE — PUBLIC METADATA INTERFACES
  %% =========================================================

  rda_oai[researchdata.se \n OAI-PMH endpoint]
  click rda_oai "https://docs.researchdata.se/harvesting/oai-pmh/" "researchdata.se OAI-PMH endpoint"

  rda_dcat@{ shape: document, label: "researchdata.se \n DCAT export"}

  rda_sitemap@{ shape: doc, label: "sitemap.xml"}

  rda_jsonld@{ shape: documents, label: "Landing page\nJSON-LD"}


  %% =========================================================
  %% DOWNSTREAM CATALOGUES
  %% =========================================================

  dataportal[dataportal.se]
  click dataportal "https://dataportal.se/" "Sweden's national data portal"

  eu_dataportal[data.europa.eu]
  click eu_dataportal "https://data.europa.eu/" "EU Data Portal"

  cessda[datacatalogue.cessda.eu]
  click cessda "https://datacatalogue.cessda.eu/" "CESSDA Data Catalogue"

  clarin_vlo[vlo.clarin.eu]
  click clarin_vlo "https://vlo.clarin.eu/" "CLARIN Virtual Language Observatory"

  ariadne[portal.ariadne-infrastructure.eu]
  click ariadne "https://portal.ariadne-infrastructure.eu/" "ARIADNE archaeology portal"

  web_crawlers["web crawlers \n (Google, Bing, etc.)"]


  %% =========================================================
  %% REPOSITORY INGESTION FLOWS
  %% =========================================================

  repo1 --> repo1_oai
  repo1_oai --> rda_harvester

  repo2 --> repo2_sitemap
  repo2 --> repo2_jsonld

  repo2_sitemap --> repo2_jsonld
  repo2_sitemap --> rda_harvester
  repo2_jsonld --> rda_harvester

  repo3 --> datacite_api
  repo4 --> datacite_api


  %% =========================================================
  %% DATACITE INGESTION FLOW
  %% =========================================================

  datacite_api --> datacite
  datacite --> datacite_oai
  datacite_oai --> rda_harvester


  %% =========================================================
  %% RESEARCHDATA.SE INTERNAL FLOW
  %% =========================================================

  rda_harvester --> rda_index
  rda_index --> rda_catalogue


  %% =========================================================
  %% RESEARCHDATA.SE EXPORT FLOWS
  %% =========================================================

  rda_catalogue --> rda_oai
  rda_catalogue --> rda_dcat
  rda_catalogue --> rda_sitemap
  rda_catalogue --> rda_jsonld

  rda_sitemap --> rda_jsonld


  %% =========================================================
  %% DOWNSTREAM HARVESTING
  %% =========================================================

  rda_dcat --> dataportal
  dataportal --> eu_dataportal

  rda_oai --> cessda
  rda_oai --> clarin_vlo
  rda_oai -. under development .-> ariadne

  rda_sitemap --> web_crawlers
  rda_jsonld --> web_crawlers
```