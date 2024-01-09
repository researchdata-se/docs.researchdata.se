# oai-pmh

The Open Archives Initiative Protocol for Metadata Harvesting (OAI-PMH) is a well estabilished specification to provide a machine accionable harvest endpoint for a respository. If DataCite is used to register DOI:s each prefix will be harvestable in thier central endpoint witch will make it harvestable by SND and other repostitories.
This is the recomended way to provide metadata to SND:s metadata catalogue.

A oai-pmh endpoint must be able describe each resource in `oai_dc` (dublin core). Additional parallell metadata formats is recomended.  
For researchdata.se DataCite XML is required.

[OAI-PMH v2.0](http://www.openarchives.org/OAI/openarchivesprotocol.html)