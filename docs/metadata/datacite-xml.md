# DataCite XML

<div class="grid cards" markdown>
-   🚧 __Draft list__

    ---

    This list of fields is a draft. 
    Discussions in the [issue tracker](https://github.com/researchdata-se/docs.researchdata.se/issues/1)  

</div>

When a DOI is registred via DataCite metadata is provided.   
This metadata is harvestable via DataCites [OAI-PMH](../harvesting/oai-pmh.md) endpoint.


## Metadata fields

_**(M):** Mandatory, **(R):** Recommended, **(O):** Optional_

### Identifier (M)

The unique identifier for this version of the resource.

#### Example
```xml
<identifier identifierType="DOI">10.123/245.67</identifier>
```
[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/identifier/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_identifier.html)

--------------

### Creator (M)

The main researchers involved in producing the resource, in priority order (occurrences: 1-n).

#### Example
```xml
<creators>
  <creator>
    <creatorName nameType="Personal">Kirchner, Nina</creatorName>
    <givenName>Nina</givenName>
    <familyName>Kirchner</familyName>
    <nameIdentifier schemeURI="https://orcid.org" nameIdentifierScheme="ORCID">0000-0002-6371-5527</nameIdentifier>
    <affiliation affiliationIdentifier="https://ror.org/05f0yaq80" affiiationIdentifierScheme="ROR" schemeURI="https://ror.org">Stockholm University</affiliation>
    <affiliation affiliationIdentifier="https://ror.org/058zxsr17" affiiationIdentifierScheme="ROR" schemeURI="https://ror.org">Bolin Centre for Climate Research</affiliation>            
  </creator>
  <creator>
    <creatorName nameType="Personal">Jansen, Joachim</creatorName>
    <givenName>Joachim</givenName>
    <familyName>Jansen</familyName>
    <nameIdentifier schemeURI="https://orcid.org" nameIdentifierScheme="ORCID">0000-0001-5965-7662</nameIdentifier>
    <affiliation affiliationIdentifier="https://ror.org/05f0yaq80" affiiationIdentifierScheme="ROR" schemeURI="https://ror.org">Stockholm University</affiliation>  
  </creator>
  <creator>
    <creatorName xml:lang="en" nameType="Organizational">Bolin Centre for Climate Research</creatorName>
    <nameIdentifier schemeURI="https://ror.org/" nameIdentifierScheme="ROR">https://ror.org/058zxsr17</nameIdentifier>
  </creator>
</creators>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/creator/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_creator.html)

--------------

### Title (M)

A name or title by which a resource is known (occurrences: 1-n).

#### Example
```xml
<titles>
  <title xml:lang="en">Example title</title>
</titles>
```
[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/title/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_title.html)

--------------
### Publisher (M)


The name of the entity that holds, archives, publishes prints, distributes, releases, issues, or produces the resource. This property will be used to formulate the citation, so consider the prominence of the role (occurrences: 1).

#### Example
```xml
<publisher xml:lang="en" publisherIdentifier="https://ror.org/058zxsr17" publisherIdentifierScheme="ROR" schemeURI="https://ror.org/">Bolin Centre for Climate Research</publisher>
```
[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/publisher/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_publisher.html)

--------------

### PublicationYear (M)

The year when the data was or will be made publicly available. (occurrences: 1)

#### Example
```xml
<publicationYear>2024</publicationYear>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/publicationyear/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_publicationyear.html)

--------------

### Subject (M)

Subject, keyword, classification code, or key phrase describing the resource (occurrences: 0-n).

#### Example
```xml
<subjects>
  <subject xml:lang="en" subjectScheme="Library of Congress Subject Headings (LCSH)" schemeURI="https://id.loc.gov/authorities/subjects.html" valueURI="https://id.loc.gov/authorities/subjects/sh85083064.html">Medicine</subject>
  <subject subjectScheme="CESSDA Topic Classification" valueURI="https://vocabularies.cessda.eu/vocabulary/TopicClassification?code=ScienceAndTechnology" classificationCode="ScienceAndTechnology" xml:lang="en">SCIENCE AND TECHNOLOGY</subject>
  <subject subjectScheme="MeSH" valueURI="http://id.nlm.nih.gov/mesh/D007091" classificationCode="D007091" xml:lang="en">Image Processing, Computer-Assisted</subject>
  <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="302" xml:lang="en">Clinical Medicine</subject>
</subjects>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/subject/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_subject.html)

--------------

### Contributor (O)

--------------
### Date (M)

--------------
### Language (R)

--------------
### ResourceType (M)

--------------
### AlternateIdentifier (O)

--------------
### RelatedIdentifier (O)

--------------
### Format (O)

--------------
### Version (O)

--------------
### Rights (R)

--------------
### Description (M)

--------------
### FundingReference (O)

Information about financial support (funding) for the resource being registered (occurrence: 0-n).

#### Example
```xml
<fundingReferences>
  <fundingReference>
    <funderName>Formas</funderName>
    <funderIdentifier funderIdentifierType="ROR">https://ror.org/03pjs1y45</funderIdentifier>
    <awardNumber awardURI="https://www.vr.se/swecris#/project/2021-02916_Formas">2021-02916</awardNumber>
    <awardTitle xml:lang="sv">Glaciärer, klimat och snabba förändringarna i det svenska Arktis - ett kommunikationsprojekt genom erfarenhetsbaserat lärande vid Tarfala forskningsstation</awardTitle>
  </fundingReference>
</fundingReferences>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/fundingreference/)

--------------

## References

- [DataCite shema documentation](http://schema.datacite.org)
- [OpenAIRE Guidelines for Data Archives](https://guidelines.openaire.eu/en/latest/data/index.html)