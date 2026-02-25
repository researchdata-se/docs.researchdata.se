# API for Researchdata.se
The official REST API for Researchdata.se is currently under development.

Additional methods are available for accessing metadata:  

* an OAI-PMH endpoint available for harvesting the metadata in multiple formats 
* a RSS feed for search results.

Information about the REST API development will be published on this page when it is available.


## OAI-PMH
All records in the catalogue are available via [OAI-PMH](https://www.openarchives.org/OAI/openarchivesprotocol.html). The OAI-PMH endpoint for harvesting metadata from Researchdata.se is:
[https://api.researchdata.se/oai-pmh](https://api.researchdata.se/oai-pmh?verb=Identify)

The following metadata formats are available:  
- `oai_dc` [Dublin Core](https://www.dublincore.org/specifications/dublin-core/dces/)  
- `datacite` [DataCite XML](https://schema.datacite.org)  
- `dcat` DCAT following the [DCAT-AP-SE 3.0 specification](https://docs.dataportal.se/dcat/en/)  
- `ddi25` [DDI-Codebook version 2.5](https://ddialliance.org/ddi-codebook#v2.5)  
- `ddi33` [DDI-Lifecycle version 3.3](https://ddialliance.org/ddi-lifecycle#v3.3)  
- `cmdi` [CMDI: Component Metadata Infrastructure](https://www.clarin.eu/content/cmdi-component-metadata-infrastructure)  

The metadata can be harvested in sets.  
Currently there are sets available for: Subjects and Research principal (organisation).

List of sets: [https://api.researchdata.se/oai-pmh?verb=ListSets](https://api.researchdata.se/oai-pmh?verb=ListSets)

## Search results as RSS feed
The search results on Researchdata.se is available as a RSS feed.
All of the filters from the search page can be used to create a RSS feed.
The feed is available in both English and Swedish:  

English : [https://researchdata.se/en/catalogue/search.rss](https://researchdata.se/en/catalogue/search.rss)  
Swedish : [https://researchdata.se/sv/catalogue/search.rss](https://researchdata.se/sv/catalogue/search.rss)

The feed can be filtered and sorted in the same way as the search page.  

Some examples:    

| Search URL | RSS Feed URL |
|------------|--------------|
| [https://researchdata.se/en/catalogue?search=health](https://researchdata.se/en/catalogue?search=health) | [https://researchdata.se/en/catalogue/search.rss?search=health](https://researchdata.se/en/catalogue/search.rss?search=health) |
| [https://researchdata.se/en/catalogue?principal=lund-university](https://researchdata.se/en/catalogue?principal=lund-university) | [https://researchdata.se/en/catalogue/search.rss?principal=lund-university](https://researchdata.se/en/catalogue/search.rss?principal=lund-university) |
| [https://researchdata.se/en/catalogue?sort=published-desc&size=50&principal=karolinska-institutet](https://researchdata.se/en/catalogue?sort=published-desc&size=50&principal=karolinska-institutet) | [https://researchdata.se/en/catalogue/search.rss?sort=published-desc&size=50&principal=karolinska-institutet](https://researchdata.se/en/catalogue/search.rss?sort=published-desc&size=50&principal=karolinska-institutet) |


