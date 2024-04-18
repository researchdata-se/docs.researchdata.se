# Shema.org JSON-LD

Its recomended to include json-ld in the html markup to make it easy for crawlers to find and parse the structured metadata.  
There is several ways to encode your metadata using JsonLd the goal of this list is to provide examples and recomendation about how to provide good metadata with a set of recomended properties.


??? example "SITES: Meteorological data from Miellejohka, 383 m a.s.l."
    ```html title="example of json-ld included in landing page html markup"
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@id": "https://meta.fieldsites.se/objects/-WyfFdj-sSgMbxhyDpMeNG-J",
        "@type": "Dataset",
        "acquireLicensePage": "https://meta.fieldsites.se/ontologies/sites/sitesLicence",
        "alternateName": "SITES_MET_ANS_MJH_20220101-20221231_L2_SH.csv",
        "contributor": null,
        "creator": {
            "name": "Abisko Scientific Research Station",
            "email": "ans-data@polar.se",
            "@type": "Organization",
            "parentOrganization": "Swedish Polar Research Secretariat",
            "@id": "https://meta.fieldsites.se/resources/stations/abisko"
        },
        "dateModified": "2024-02-09T10:30:09.159036Z",
        "datePublished": "2024-02-09",
        "description": "Automatic weather station data from locations within the distributed Swedish research infrastructure SITES. Check preview or file for the specific parameters included at this location. Data has been quality controlled and cleaned from outliers and other events producing unrealistic data. Gaps have not been filled.\nAbisko Scientific Research Station (2024). Meteorological data from Miellejohka, 383 m a.s.l., 2022 [Data set]. Swedish Infrastructure for Ecosystem Science (SITES). https://hdl.handle.net/11676.1/-WyfFdj-sSgMbxhyDpMeNG-J",
        "distribution": {
            "contentSize": "2192810 B",
            "contentUrl": "https://data.fieldsites.se/licence_accept?ids=%5B%22-WyfFdj-sSgMbxhyDpMeNG-JPHP_6kM5eNNQntTO_qY%22%5D",
            "encodingFormat": "text/csv",
            "sha256": "f96c9f15d8feb1280c6f18720e931e346f893c73ffea433978d3509ed4cefea6"
        },
        "identifier": "https://hdl.handle.net/11676.1/-WyfFdj-sSgMbxhyDpMeNG-J",
        "inLanguage": {
            "@type": "Language",
            "name": "English"
        },
        "includedInDataCatalog": {
            "@type": "DataCatalog",
            "name": "data.fieldsites.se"
        },
        "isBasedOn": {
            "@type": "CreativeWork",
            "name": "Previous version",
            "url": "https://meta.fieldsites.se/objects/X5DYTJ5gnPIxfjnZDr_yLssT"
        },
        "isPartOf": null,
        "keywords": ["Air temperature", "Atmospheric radiation", "Humidity", "Precipitation", "Surface Winds"],
        "license": "Some(https://creativecommons.org/licenses/by/4.0)",
        "name": "Meteorological data from Miellejohka, 383 m a.s.l., 2022",
        "producer": null,
        "provider": {
            "@type": "Organization",
            "@id": "https://meta.fieldsites.se/resources/stations/abisko",
            "name": "Abisko Scientific Research Station",
            "email": "ans-data@polar.se"
        },
        "publisher": {
            "@id": "data.fieldsites.se",
            "@type": "Organization",
            "logo": "https://static.icos-cp.eu/images/sites-logo.png",
            "name": "SITES data portal",
            "url": "https://data.fieldsites.se"
        },
        "spatialCoverage": [{
            "@type": "Place",
            "containedInPlace": {
            "@type": "Country",
            "identifier": "SE",
            "name": "Sweden"
            },
            "geo": {
            "@type": "GeoCoordinates",
            "latitude": 68.346,
            "longitude": 18.955
            },
            "name": "Miellejohka, 383 m a.s.l."
        }, {
            "@type": "Place",
            "containedInPlace": {
            "@type": "Country",
            "identifier": "SE",
            "name": "Sweden"
            },
            "geo": {
            "@type": "GeoShape",
            "polygon": "68.318339 18.911518 68.319197 18.910572 68.320464 18.910522 68.32114 18.91387 68.322182 18.913514 68.323466 18.917356 68.324513 18.917536 68.325752 18.921006 68.327912 18.923129 68.330305 18.923395 68.332761 18.927077 68.334287 18.92559 68.335532 18.92651 68.336531 18.926074 68.337713 18.929658 68.339064 18.929527 68.340235 18.931286 68.34159 18.930985 68.341853 18.932417 68.342284 18.932807 68.342585 18.929576 68.34404 18.930338 68.344209 18.93117 68.345168 18.930144 68.34617 18.943988 68.346379 18.951858 68.346094 18.952903 68.346506 18.954458 68.346771 18.958445 68.346298 18.958679 68.346061 18.96146 68.346681 18.962225 68.346745 18.963671 68.346225 18.963629 68.346331 18.964864 68.346032 18.965347 68.344687 18.965234 68.344526 18.963673 68.343146 18.963141 68.34267 18.963909 68.341427 18.963668 68.339656 18.966716 68.338714 18.965165 68.336773 18.964413 68.335853 18.962648 68.334877 18.962527 68.334359 18.963142 68.334104 18.96407 68.334279 18.964635 68.333808 18.96555 68.332325 18.966337 68.331996 18.965817 68.329965 18.966193 68.329301 18.967657 68.32723 18.969727 68.326828 18.971163 68.326377 18.970866 68.325119 18.972372 68.323152 18.979878 68.322173 18.978735 68.322275 18.976711 68.321749 18.976158 68.321612 18.975138 68.320724 18.975055 68.319932 18.973629 68.318362 18.975007 68.31847 18.972742 68.319171 18.970119 68.318923 18.968472 68.318852 18.962361 68.319239 18.960485 68.318978 18.95784 68.319312 18.956999 68.318578 18.955 68.318403 18.952176 68.319052 18.94755 68.319141 18.945671 68.318882 18.944484 68.319392 18.933153 68.31915 18.932382 68.319337 18.931709 68.318781 18.924422 68.318955 18.923893 68.318533 18.923869 68.318699 18.921784 68.316612 18.919602 68.317691 18.919594 68.317576 18.918748 68.31832 18.917272 68.318543 18.913545"
            },
            "name": "Miellejohka Sub-Alpine"
        }],
        "temporalCoverage": "2021-12-31T23:10:00Z/2022-12-31T23:00:00Z",
        "url": "https://meta.fieldsites.se/objects/-WyfFdj-sSgMbxhyDpMeNG-J",
        "variableMeasured": [{
            "@type": "PropertyValue",
            "description": "Time instant",
            "name": "TIMESTAMP",
            "unitText": null
        }, {
            "@type": "PropertyValue",
            "description": "Air temperature",
            "name": "TA",
            "unitText": "°C"
        }, {
            "@type": "PropertyValue",
            "description": "Air temperature",
            "name": "TA_2",
            "unitText": "°C"
        }, {
            "@type": "PropertyValue",
            "description": "Relative humidity",
            "name": "RH",
            "unitText": "%"
        }]
    }
	</script>
    ```


## Properties

To describe a dateset using schema.org the json-ld type must be set to `Dataset` minimal example:

??? example "Minimal JsonLD Dataset"
    ```json title="example of json-ld included in landing page html markup"
    {
        "@context": "https://schema.org/",
        "@id": "https://doi.org/xxxx",
        "@type": "Dataset",
        "name": "Example dataset",
        "description": "Dataset description",
        "keywords": ["example tag", "another tag"],
        "publisher": {
            "@type": "Organization",
            "@id": "https://ror.org/0093a8w51"
            "name": "Blekinge Institute of Technology"
        }
    }
    ```
For the proerty examples only the value will be listed to make the examples a bit shorter.

### identifier

Single or multiple values for identifiers for local or global identifiers for the dataset.
Can be `text`, `url` or a set of `PropertyValue` 

### creator

#### Example
```json title="list of creators"
[
    {
        "@type": "Person",
        "@id": "https://orcid.org/0000-0002-7365-0691",
        "givenName": "Olof",
        "familyName": "Olsson"
    },
    {
        "@type": "Organization",
        "@id": "https://ror.org/048a87296",
        "name": "Uppsala University"
    }
]
```

One or multiple [Organization]() and/or [Person]()

[Reference](https://schema.org/creator)

### name

Used for the title of the dataset, an alternate title exist use the property `alternateName`

### publisher

Recomended to use a single organization.

### datePublished

Examples:
`2024-04-01`  
`2024`

ISO-8601 date, full date or just year.

### dateCreated

Examples:
`2024-04-01`  
`2024`

ISO-8601 date, full date or just year.

### keywords

### contributor

### inLanguage

### additionalType

### version

Version number of the dataset if availible.

Examples:  
`1`
`1.0`

### license

URL to the licence for the dataset.

Examples:  
`https://creativecommons.org/publicdomain/zero/1.0/`  
`https://creativecommons.org/licenses/by/4.0/`


### description

### distribution

Describes and links to the files in the dataset.

```json title="list of files in the dataset"
[
    {
        "@type": "DataDownload",
        "name": "my-data.tsv",
        "contentUrl": "https://www.sample-data-repository.org/dataset/my-data.csv",
        "encodingFormat": "text/csv"
    },
    {
        "@type": "DataDownload",
        "name": "readme.txt",
        "contentUrl": "https://www.sample-data-repository.org/dataset/readme.txt",
        "encodingFormat": "text/plain"
    }
]
```
[Reference](https://schema.org/distribution)

### spatialCoverage

### funding

## Examples



    
## References

- [Shema.org/Dataset](https://schema.org/Dataset)
- [Schema.org validator](https://validator.schema.org)
- [Google Dataset structured data](https://developers.google.com/search/docs/appearance/structured-data/dataset)