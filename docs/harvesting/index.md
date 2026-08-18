# Introduction

For Researchdata.se to be able to harvest dataset metadata from a data source such as a repository, a machine actionable way to access the metadata is needed.

To avoid a Researchdata.se-specific method, we recommend using established metadata standards like DataCite XML via [OAI-PMH](oai-pmh.md) and/or Schema.org JSON-LD one the landing page via [sitemap.xml](sitemap-xml.md).

## Harvesting flow 
Metadata from national research data repositories is harvested and made available to other data portals and search engines.  
The figure below illustrates the harvesting flow.


``` mermaid
graph
  RDA[(researchdata.se \n elasticsearch)]
  RDAC[researchdata.se \n catalogue]
  click RDAC "https://researchdata.se/" "researchdata.se catalogue"
  
  DATACITE[(DataCite)]
  DATACITEOAI[DataCite\nOAI-PMH endpoint]
  click DATACITEOAI "https://support.datacite.org/docs/datacite-oai-pmh" "DataCite OAI-PMH endpoint"
  DATACITEAPI[DataCite API]
  click DATACITEAPI "https://support.datacite.org/docs/api" "DataCite API"
  DATACITE --> DATACITEOAI
  DATACITEAPI --> DATACITE

  DATACITEOAI --> RDAH


  RP1[(Repository 1)]
  OAI1[Repository 1 \n OAI-PMH endpoint]

  RP3[(Repository 3)]
  RP3 --> DATACITEAPI

  RP4[(Repository 4)]
  RP4 --> DATACITEAPI

  RP2[(Repository 2)]
  LDSM2@{ shape: doc, label: "sitemap.xml"}
  RP2 --> LDLP2
  LDLP2@{ shape: documents, label: "Landing page \nJSON-LD"}

  RDAH@{ shape: procs, label: "researchdata.se \n harvester"}

  RDAOAI[researchdata.se \n OAI-PMH endpoint]
  click RDAOAI "https://docs.researchdata.se/harvesting/oai-pmh/" "researchdata.se OAI-PMH endpoint"
  RDAC --> RDAOAI

  RDACDCAT@{ shape: document, label: "researchdata.se \n DCAT export"}
  RDAC --> RDACDCAT

  RDACATLD@{ shape: documents, label: "Landing page\nJSON-LD"}
  RDAC --> RDACATLD

  DATAPORTAL[dataportal.se]
  click DATAPORTAL "https://dataportal.se/" "Sweden's national data portal"
  RDACDCAT --> DATAPORTAL

  EUDATAPORTAL[data.europa.eu]
  click EUDATAPORTAL "https://data.europa.eu/" "EU Data Portal"
  DATAPORTAL --> EUDATAPORTAL

  CESSDA[datacatalogue.cessda.eu]
  click CESSDA "https://datacatalogue.cessda.eu/" "CESSDA Data Catalogue"
  RDAOAI --> CESSDA

  CLARINVLO[vlo.clarin.eu]
  click CLARINVLO "https://vlo.clarin.eu/" "CLARIN Virtual Language Observatory"
  RDAOAI --> CLARINVLO

  ARIADNE[portal.ariadne-infrastructure.eu]
  click ARIADNE "https://portal.ariadne-infrastructure.eu/" "ARIADNE archaeology portal"
  RDAOAI -. under development .-> ARIADNE

  RDACSITEMAP@{ shape: doc, label: "sitemap.xml"}
  RDAC --> RDACSITEMAP
  RDACSITEMAP --> RDACATLD

  WEBCRAWLERS["web crawlers \n (Google, Bing, etc.)"]
  RDACSITEMAP --> WEBCRAWLERS
  RDACATLD --> WEBCRAWLERS

  RP1 --> OAI1
  OAI1 --> RDAH

  RP2 --> LDSM2
  LDSM2 --> LDLP2
  LDSM2 --> RDAH
  LDLP2 --> RDAH

  RDAH --> RDA
  RDA --> RDAC
```