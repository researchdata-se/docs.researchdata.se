# DataCite XML

<div class="grid cards" markdown>
-   🚧 __Draft list__

    ---

    This list of fields is a draft. 
    Discussions in the [issue tracker](https://github.com/researchdata-se/docs.researchdata.se/issues/1)  

</div>

When a DOI is registred via DataCite metadata is provided.   
This metadata is harvestable via DataCites [OAI-PMH](../harvesting/oai-pmh.md) endpoint.

**(M):** Mandatory, **(R):** Recommended, **(O):** Optional  

## Metadata fields

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

--------------
### Publisher (M)

--------------
### PublicationYear (M)

--------------
### Subject (M)

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