# API for researchdata.se
The official REST API for researchdata.se is currently under development but there is a OAI-PMH endpoint available for harvesting the metadata in multiple formats and a RSS feed for search results.

Information about the REST API development will be published on this page when it is available.


## OAI-PMH
All records in the catalogue are available via [OAI-PMH](https://www.openarchives.org/OAI/openarchivesprotocol.html). The OAI-PMH endpoint for harvesting metadata from researchdata.se is:
[https://api.researchdata.se/oai-pmh](https://api.researchdata.se/oai-pmh?verb=Identify)

The following metadata formats are available:  
- `oai_dc` [Dublin Core](https://www.dublincore.org/specifications/dublin-core/dces/)  
- `datacite` [DataCite XML](https://schema.datacite.org)  
- `dcat` DCAT following the [DCAT-AP-SE 3.0 specification](https://docs.dataportal.se/dcat/en/)  
- `ddi25` [DDI-C 2.5](https://ddialliance.org/ddi-codebook#v2.5)  
- `ddi33` [DDI-L 3.3](https://ddialliance.org/ddi-lifecycle#v3.3)  

The metadata can be harvested in sets.  
Currently there is sets availible for: subjects and research principal organization.

List of sets: [https://api.researchdata.se/oai-pmh?verb=ListSets](https://api.researchdata.se/oai-pmh?verb=ListSets)

## Search results as RSS feed
The search results on researchdata.se is available as a RSS feed.
All the filters from the search page can be used to create a RSS feed.
The feed is availible in both english and swedish:   
English : [https://researchdata.se/en/catalogue/search.rss](https://researchdata.se/en/catalogue/search.rss)  
Swedish : [https://researchdata.se/sv/catalogue/search.rss](https://researchdata.se/sv/catalogue/search.rss)

The feed can be filtered and sorted in the same way as the search page.  

Some examples:    

| Search URL | RSS Feed URL |
|------------|--------------|
| [https://researchdata.se/en/catalogue?search=health](https://researchdata.se/en/catalogue?search=health) | [https://researchdata.se/en/catalogue/search.rss?search=health](https://researchdata.se/en/catalogue/search.rss?search=health) |
| [https://researchdata.se/en/catalogue?principal=lund-university](https://researchdata.se/en/catalogue?principal=lund-university) | [https://researchdata.se/en/catalogue/search.rss?principal=lund-university](https://researchdata.se/en/catalogue/search.rss?principal=lund-university) |
| [https://researchdata.se/en/catalogue?sort=published-desc&size=50&principal=karolinska-institutet](https://researchdata.se/en/catalogue?sort=published-desc&size=50&principal=karolinska-institutet) | [https://researchdata.se/en/catalogue/search.rss?sort=published-desc&size=50&principal=karolinska-institutet](https://researchdata.se/en/catalogue/search.rss?sort=published-desc&size=50&principal=karolinska-institutet) |


