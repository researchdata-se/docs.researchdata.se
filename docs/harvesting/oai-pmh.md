# oai-pmh

The Open Archives Initiative Protocol for Metadata Harvesting (OAI-PMH) is a well estabilished specification to provide a machine accionable harvest endpoint for a respository. If DataCite is used to register DOI:s each prefix will be harvestable in thier central endpoint witch will make it harvestable by researchdata.se and other repostitories.
This is the recomended way to provide metadata to the catalogue on researchdata.se.

A oai-pmh endpoint must be able describe each resource in `oai_dc` (dublin core). Additional parallell metadata formats is recomended.  
For researchdata.se [DataCite XML](../metadata/datacite-xml.md) is required.

## OAI-PMH via DataCite
If the repository registers DOI:s via DataCite all metadata will be harvestable via a OAI-PMH set on `oai.datacite.org` some example sets:  

* [SND.SND via DataCite](https://oai.datacite.org/oai/?verb=ListRecords&metadataPrefix=datacite&set=SND.SND)
* [SND.BOLIN via DataCite](https://oai.datacite.org/oai/?verb=ListRecords&metadataPrefix=datacite&set=SND.BOLIN)



### References

* [OAI-PMH v2.0 specification](http://www.openarchives.org/OAI/openarchivesprotocol.html)
* [DataCite OAI-PMH guide](https://support.datacite.org/docs/datacite-oai-pmh)
