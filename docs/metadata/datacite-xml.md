# DataCite XML

When a DOI is registred via DataCite metadata is provided.   
This metadata is harvestable via DataCites [OAI-PMH](../harvesting/oai-pmh.md) endpoint.


## Metadata fields

_**(M):** Mandatory, **(R):** Recommended, **(O):** Optional_

### Identifier (M)

The unique identifier for this version of the resource.

```xml title="identifier example"
<identifier identifierType="DOI">10.123/245.67</identifier>
```
[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/identifier/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_identifier.html)

--------------

### Creator (M)

The person(-s) and/or organization(-s) involved in creating the resource, in priority order (occurrences: 1-n).

```xml title="creator example"
<creators>
  <creator>
    <creatorName nameType="Personal">Kirchner, Nina</creatorName>
    <givenName>Nina</givenName>
    <familyName>Kirchner</familyName>
    <nameIdentifier schemeURI="https://orcid.org" nameIdentifierScheme="ORCID">0000-0002-6371-5527</nameIdentifier>
    <affiliation affiliationIdentifier="https://ror.org/05f0yaq80" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org">Stockholm University</affiliation>
    <affiliation affiliationIdentifier="https://ror.org/058zxsr17" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org">Bolin Centre for Climate Research</affiliation>            
  </creator>
  <creator>
    <creatorName nameType="Personal">Jansen, Joachim</creatorName>
    <givenName>Joachim</givenName>
    <familyName>Jansen</familyName>
    <nameIdentifier schemeURI="https://orcid.org" nameIdentifierScheme="ORCID">0000-0001-5965-7662</nameIdentifier>
    <affiliation affiliationIdentifier="https://ror.org/05f0yaq80" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org">Stockholm University</affiliation>  
  </creator>
  <creator>
    <creatorName xml:lang="en" nameType="Organizational">Bolin Centre for Climate Research</creatorName>
    <nameIdentifier schemeURI="https://ror.org/" nameIdentifierScheme="ROR">https://ror.org/058zxsr17</nameIdentifier>
  </creator>
</creators>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/creator/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_creator.html)

--------------

### Title (M)

A name or title by which a resource is known (occurrences: 1-n).

```xml title="title example"
<titles>
  <title xml:lang="en">Example title</title>
</titles>
```
[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/title/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_title.html)

--------------

### Publisher (M)


The name of the entity that holds, archives, publishes prints, distributes, releases, issues, or produces the resource. This property will be used to formulate the citation, so consider the prominence of the role (occurrences: 1).

```xml title="publisher example"
<publisher xml:lang="en" publisherIdentifier="https://ror.org/058zxsr17" publisherIdentifierScheme="ROR" schemeURI="https://ror.org/">Bolin Centre for Climate Research</publisher>
```
[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/publisher/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_publisher.html)

--------------

### PublicationYear (M)

The year when the resource was or will be made publicly available. (occurrences: 1)

```xml title="publicationYear example"
<publicationYear>2024</publicationYear>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/publicationyear/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_publicationyear.html)

--------------

### Subject (M)

Subject, keyword, classification code, or key phrase describing the resource (occurrences: 0-n).

```xml title="subject example"
<subjects>
  <subject xml:lang="en" subjectScheme="Library of Congress Subject Headings (LCSH)" schemeURI="https://id.loc.gov/authorities/subjects.html" valueURI="https://id.loc.gov/authorities/subjects/sh85083064.html">Medicine</subject>
  <subject subjectScheme="CESSDA Topic Classification" valueURI="https://vocabularies.cessda.eu/vocabulary/TopicClassification?code=ScienceAndTechnology" classificationCode="ScienceAndTechnology" xml:lang="en">SCIENCE AND TECHNOLOGY</subject>
  <subject subjectScheme="MeSH" valueURI="http://id.nlm.nih.gov/mesh/D007091" classificationCode="D007091" xml:lang="en">Image Processing, Computer-Assisted</subject>
  <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="302" xml:lang="en">Clinical Medicine</subject>
</subjects>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/subject/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_subject.html)

--------------

### Contributor (O)

The institution or person responsible for collecting, managing, distributing, or otherwise contributing to the development of the resource. To supply multiple contributors, repeat this property. (occurrence: 0-n)

```xml title="contributor example"
<contributors>
  <contributor contributorType="Other">
    <contributorName nameType="Personal">Kirchner, Nina</creatorName>
    <givenName>Nina</givenName>
    <familyName>Kirchner</familyName>
    <nameIdentifier schemeURI="https://orcid.org" nameIdentifierScheme="ORCID">0000-0002-6371-5527</nameIdentifier>
    <affiliation affiliationIdentifier="https://ror.org/05f0yaq80" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org">Stockholm University</affiliation>          
  </contributor>
</contributors>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/contributor/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_contributor.html)

--------------

### Date (M)

Different dates relevant to the work (occurrences: 0-n).  
Coverage date is defined as a date span separated by `/`.  
List of dateType: [dateTypes at datacite](https://datacite-metadata-schema.readthedocs.io/en/4.6/appendices/appendix-1/dateType/)

```xml title="date example"
<dates>
  <date dateType="Issued">2024-01-05</date>
  <date dateType="Coverage">2022-08-01/2025-01-02</date>
</dates>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/date/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_date.html)

--------------

### Language (R)

The primary language of the resource (occurrences: 0-1).  
ISO 639-3 language codes. Examples: `eng`, `swe`, `deu`.

```xml  title="language example"
<language>eng</language>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/language/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_language.html)

--------------

### ResourceType (M)

A description of the resource (occurrences: 0-1).

```xml title="resourceType example"
<resourceType resourceTypeGeneral="Dataset">Dataset</resourceType>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/resourcetype/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_resourcetype.html)

--------------

### AlternateIdentifier (O)

An identifier or identifiers other than the primary Identifier applied to the resource being registered (occurrences: 0-n).

```xml title="alternateIdentifier example"
<alternateIdentifiers>
  <alternateIdentifier alternateIdentifierType="ISBN">937-0-1234-56789-X</alternateIdentifier>
</alternateIdentifiers>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/alternateidentifier/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_alternateidentifier.html)

--------------

### RelatedIdentifier (O)

Identifiers of related resources. These must be globally unique identifiers (occurrences: 0-n).

```xml title="relatedIdentifier example"
<relatedIdentifiers>
  <relatedIdentifier relatedIdentifierType="DOI" relationType="IsCitedBy" resourceTypeGeneral="JournalArticle">10.21384/bar</relatedIdentifier>
  <relatedIdentifier relatedIdentifierType="DOI" relationType="IsNewVersionOf" resourceTypeGeneral="Dataset">10.21384/123.456</relatedIdentifier>
</relatedIdentifiers>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/relatedidentifier/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_relatedidentifier.html)


--------------

### Format (O)

Technical format of the resource. (occurrences: 0-n).

```xml title="format example"
<formats>
  <format>text/csv</format>
</formats>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/format/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_format.html)

--------------

### Version (O)

The version number of the resource (occurrences: 0-1).

```xml title="version example"
<version>2</version>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/version/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_version.html)


--------------
### Rights (R)

Any rights information for this resource (occurrences: 0-n).  
Its recomended to describe the access level by using [info:eu-repo-Access-Terms vocabulary](https://guidelines.openaire.eu/en/latest/data/field_rights.html#rightsuri-ma).

```xml title="rights example"
<rightsList>
  <rights rightsURI=”info:eu-repo/semantics/openAccess” />
  <rights rightsURI=”http://creativecommons.org/licenses/by/4.0/”>
    Creative Commons Attribution 4.0 International
  </rights>
</rightsList>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/rights/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_rights.html)

--------------

### Description (M)

A brief summary of the resource. May also be used for technical information. (occurrences: 0-n).

```xml title="description example"
<descriptions>
  <description xml:lang="en" descriptionType="Abstract">
    Example description.
  </description>
  <description xml:lang="sv" descriptionType="Abstract">
    Exempelbeskrivning.
  </description>
  <description xml:lang="en" descriptionType="Other">
    This is a note or some extra description.
  </description>
</descriptions>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/description/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_description.html)

--------------

### GeoLocation (O)

Spatial region or named place where the data contained in the resource was gathered or about which the data is focused (occurrences: 0-n).

```xml title="GeoLocation example"
<geoLocations>
  <geoLocation>
    <geoLocationPoint>31.233 -67.302</geoLocationPoint>
    <geoLocationBox>41.090 -71.032 42.893 -68.211</geoLocationBox>
    <geoLocationPlace>Atlantic Ocean</geoLocationPlace>
  </geoLocation>
</geoLocations>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/geolocation/) |
[OpenAIRE](https://guidelines.openaire.eu/en/latest/data/field_geolocation.html)


--------------

### FundingReference (O)

Information about financial support (funding) for the resource being registered (occurrence: 0-n).

```xml title="fundingReference example"
<fundingReferences>
  <fundingReference>
    <funderName>Formas</funderName>
    <funderIdentifier funderIdentifierType="ROR">https://ror.org/03pjs1y45</funderIdentifier>
    <awardNumber awardURI="https://www.vr.se/swecris#/project/2021-02916_Formas">2021-02916</awardNumber>
    <awardTitle xml:lang="sv">Glaciärer, klimat och snabba förändringarna i det svenska Arktis - ett kommunikationsprojekt genom erfarenhetsbaserat lärande vid Tarfala forskningsstation</awardTitle>
  </fundingReference>
</fundingReferences>
```

[Specification](https://datacite-metadata-schema.readthedocs.io/en/4.6/properties/fundingreference/)

--------------

## References

- [DataCite schema documentation](http://schema.datacite.org)
- [OpenAIRE Guidelines for Data Archives](https://guidelines.openaire.eu/en/latest/data/index.html)
- [DataCite validate metadata](https://support.datacite.org/docs/how-do-i-validate-doi-metadata)
