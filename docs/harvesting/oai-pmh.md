# OAI-PMH

The _Open Archives Initiative Protocol for Metadata Harvesting_ (OAI-PMH) is a well established specification for providing a machine actionable harvesting endpoint for a repository.

If DataCite is used to register DOI:s, each DOI prefix will be harvestable using DataCites central endpoint, thus making it harvestable by researchdata.se and other aggregators.


This is the recommended way to provide metadata to the Researchdata.se catalogue.

An OAI-PMH endpoint must be able to describe each resource in `oai_dc` (Dublin Core). Delivery of additional metadata formats in parallel is recommended.  

For Researchdata.se, [DataCite XML](../metadata/datacite-xml.md) is required.

## Researchdata.se OAI-PMH endpoint
The OAI-PMH endpoint for harvesting metadata from Researchdata.se is:  
[https://api.researchdata.se/oai-pmh](https://api.researchdata.se/oai-pmh?verb=Identify)

## OAI-PMH via DataCite
If the repository registers DOI:s via DataCite, all metadata will be harvestable via a OAI-PMH set on `oai.datacite.org`.

Some example sets:  

* [SND.SND via DataCite](https://oai.datacite.org/oai/?verb=ListRecords&metadataPrefix=datacite&set=SND.SND)
* [SND.BOLIN via DataCite](https://oai.datacite.org/oai/?verb=ListRecords&metadataPrefix=datacite&set=SND.BOLIN)



### References

* [OAI-PMH v2.0 specification](http://www.openarchives.org/OAI/openarchivesprotocol.html)
* [DataCite OAI-PMH guide](https://support.datacite.org/docs/datacite-oai-pmh)