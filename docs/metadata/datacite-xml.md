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
        <creatorName nameType="Personal">Anka, Kalle</creatorName>
        <givenName>Kalle</givenName>
        <familyName>Anka</familyName>
        <nameIdentifier schemeURI="https://orcid.org/" nameIdentifierScheme="ORCID">0000-0001-5727-2427</nameIdentifier>
        <affiliation affiliationIdentifier="https://ror.org/03efmqc40" affiiationIdentifierScheme="ROR" schemeURI="https://ror.org">Arizona State University</affiliation>
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
### AlternateIdentifier (M)

--------------
### RelatedIdentifier (M)

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

--------------

## References

- [DataCite shema documentation](http://schema.datacite.org)
- [OpenAIRE Guidelines for Data Archives](https://guidelines.openaire.eu/en/latest/data/index.html)