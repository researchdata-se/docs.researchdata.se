# Introduction

For Researchdata.se to be able to harvest dataset metadata from a data source such as a repository, a machine actionable way to access the metadata is needed.

To avoid a Researchdata.se-specific method, we recommend using established metadata standards like DataCite XML via [OAI-PMH](oai-pmh.md) and/or Schema.org JSON-LD one the landing page via [sitemap.xml](sitemap-xml.md).

## Harvesting flow 
*(work in progress)*


``` mermaid
graph
  RDA[(RDA \n elasticsearch)]
  RDAC[researchdata.se]
  
  DS[(DataCite)]
  DSOAI[DataCite\nOAI-PMH endpoint]
  DSAPI[DataCite API]
  DS --> DSOAI
  DSAPI --> DS

  DSOAI --> RDAH


  RP1[(Repository 1)]
  OAI1[OAI-PMH endpoint]

  RP3[(Repository 3)]
  RP3 --> DSAPI

  RP4[(Repository 4)]
  RP4 --> DSAPI

  RP2[(Repository 2)]
  LDSM2[sitemap.xml]
  LDLP2[Landing page \nJsonLD]

  RDAH[RDA harvester]

  RP1 --> OAI1
  OAI1 --> RDAH

  RP2 --> LDSM2
  LDSM2 --> LDLP2
  LDSM2 --> RDAH
  LDLP2 --> RDAH

  RDAH --> RDA
  RDA --> RDAC
```