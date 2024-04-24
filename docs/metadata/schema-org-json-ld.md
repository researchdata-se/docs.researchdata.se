# Shema.org JSON-LD

Its recomended to include json-ld in the html markup to make it easy for crawlers to find and parse the structured metadata.  
There is several ways to encode your metadata using JsonLd the goal of this list is to provide examples and recomendation about how to provide good metadata with a set of recomended properties.

## Properties

To describe a dateset using schema.org the json-ld type must be set to `Dataset` minimal example:

??? example "Minimal JsonLD Dataset"
    ```html title="example of JsonLd included in landing page html markup"
    <script type="application/ld+json">
    {
        "@context":"https://schema.org/",
        "@type":"Dataset",
        "@id":"https://doi.org/xxxx",
        "name":"Example dataset",
        "description":"Dataset description",
        "keywords":[
            "example tag",
            "another tag"
        ],
        "publisher":{
            "@type":"Organization",
            "@id":"https://ror.org/0093a8w51",
            "name":"Blekinge Institute of Technology"
        }
    }
    </script>
    ```
For the proerty examples only the value will be listed to make the examples a bit shorter.

### identifier

Single or multiple values for identifiers for local or global identifiers for the dataset.
Can be `text`, `url` or a set of `PropertyValue` 

### creator

Example  
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

Used for the title of the dataset, an alternate title exist use the property `alternateName`.

### publisher

Recomended to use a single organization. 
The `@id` and/or `indetifier` should be ROR-id if availible.

```json title="publisher example"
{
    "@type": "Organization",
    "@id": "https://ror.org/048a87296",
    "name": "Uppsala University"
}
```

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

Keywords used to categorize the dataset. Values can be both text and URL:s.

Example:  
```json title="keyword example"
[
    "Health",
    "http://id.nlm.nih.gov/mesh/D014943"
]
```

### contributor

`TODO: add description & examples`

### inLanguage

`TODO: add description & examples`

### additionalType

One or multiple additional types to classify the dataset. Can be Url:s or plain text.

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

Plain text description of the dataset. Should contains a short abstract and any general technical information about the dataset.

### distribution

Describes and links to the files in the dataset.  
If the dataset contains multiple files in a hierarchical structure provide the relative path in `name`. e.g. `images/2024-03-14.jpg`.

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

`TODO: add description & examples`

### temporalCoverage

`TODO: recomendation about timespan, historical dates etc.`

Examples  
`2024-03-15` sigle date no timespan  
`2020/2024` timespan from 2020 until 2024  
`2020/..` from 2020 open ended  
`http://n2t.net/ark:/99152/p0qhb66skwk` "stenålder 10200 BP (2000) – 3800 BP (2000) | Sweden" by refering to a specified time period from [perio.do](https://perio.do)


### funding

`TODO: add description & examples`

### variableMeasured

Describes the variables in the dataset.

```json title="example variables"
[
  {
    "@type": "PropertyValue",
    "description": "Time instant",
    "name": "TIMESTAMP",
    "unitText": null
  }, 
  {
    "@type": "PropertyValue",
    "description": "Discharge",
    "name": "Q",
    "unitText": "m3 s-1"
  }
]
```

## Examples

??? example "Water balance - stream discharge from Åhedbäcken, Catchment 14, 2008-04-23–2017-10-31"
    ```html title="example of json-ld included in landing page html markup"
    {
    "@context":"https://schema.org",
    "@id":"https://meta.fieldsites.se/objects/kyCDtIXhWr-xJcyah0_hOyBt",
    "@type":"Dataset",
    "acquireLicensePage":"https://meta.fieldsites.se/ontologies/sites/sitesLicence",
    "alternateName":"SITES_WB-Q_SVB_AHB-C14_20080423-20171031_L2_30min.csv",
    "contributor":null,
    "creator":{
        "name":"Svartberget Research Station",
        "email":"data@fieldsites.se",
        "@type":"Organization",
        "parentOrganization":"Swedish University of Agricultural Sciences",
        "@id":"https://meta.fieldsites.se/resources/stations/Svartberget"
    },
    "dateModified":"2024-03-28T10:03:19.017745Z",
    "datePublished":"2024-03-28",
    "description":"Discharge calculations based on stream level measurements and a constantly validated stream discharge relation curve. For detailed information on calculations and installation read COMMENT in the header of the data set, which guides to related information document.\nSvartberget Research Station (2024). Water balance - stream discharge from Åhedbäcken, Catchment 14, 2008-04-23–2017-10-31 [Data set]. Swedish Infrastructure for Ecosystem Science (SITES). https://hdl.handle.net/11676.1/kyCDtIXhWr-xJcyah0_hOyBt",
    "distribution":{
        "contentSize":"4429994 B",
        "contentUrl":"https://data.fieldsites.se/licence_accept?ids=%5B%22kyCDtIXhWr-xJcyah0_hOyBtI_dhh2s79ZOvOk_fNc8%22%5D",
        "encodingFormat":"text/csv",
        "sha256":"932083b485e15abfb125cc9a874fe13b206d23f761876b3bf593af3a4fdf35cf"
    },
    "identifier":"https://hdl.handle.net/11676.1/kyCDtIXhWr-xJcyah0_hOyBt",
    "inLanguage":{
        "@type":"Language",
        "name":"English"
    },
    "includedInDataCatalog":{
        "@type":"DataCatalog",
        "name":"data.fieldsites.se"
    },
    "isBasedOn":null,
    "isPartOf":null,
    "keywords":[
        "Discharge",
        "Stream"
    ],
    "license":"https://meta.fieldsites.se/ontologies/sites/sitesLicence",
    "name":"Water balance - stream discharge from Åhedbäcken, Catchment 14, 2008-04-23–2017-10-31",
    "producer":null,
    "provider":{
        "@type":"Organization",
        "@id":"https://meta.fieldsites.se/resources/stations/Svartberget",
        "name":"Svartberget Research Station",
        "email":"data@fieldsites.se"
    },
    "publisher":{
        "@id":"data.fieldsites.se",
        "@type":"Organization",
        "logo":"https://static.icos-cp.eu/images/sites-logo.png",
        "name":"SITES data portal",
        "url":"https://data.fieldsites.se"
    },
    "spatialCoverage":[
        {
            "@type":"Place",
            "containedInPlace":{
                "@type":"Country",
                "identifier":"SE",
                "name":"Sweden"
            },
            "geo":{
                "@type":"GeoCoordinates",
                "latitude":64.226154,
                "longitude":19.770768
            },
            "name":"Åhedbäcken, Catchment 14"
        },
        {
            "@type":"Place",
            "containedInPlace":{
                "@type":"Country",
                "identifier":"SE",
                "name":"Sweden"
            },
            "geo":{
                "@type":"GeoShape",
                "polygon":"64.272104 19.708036 64.271311 19.709164 64.271214 19.711114 64.270884 19.711687 64.271156 19.713275 64.269577 19.715222 64.269301 19.718799 64.269808 19.721661 64.269093 19.723213 64.269149 19.724461 64.268853 19.725452 64.267816 19.727268 64.267229 19.727391 64.266785 19.728878 64.264817 19.731904 64.263942 19.732709 64.26338 19.731906 64.261923 19.732629 64.26071 19.735969 64.259687 19.735616 64.260238 19.736831 64.260062 19.738355 64.259338 19.738562 64.25895 19.739643 64.257798 19.740718 64.257647 19.742969 64.256054 19.745427 64.255548 19.747524 64.25554 19.749485 64.255057 19.750759 64.254053 19.751338 64.25388 19.752759 64.253404 19.752072 64.252406 19.752446 64.252123 19.752922 64.251973 19.755172 64.251441 19.754889 64.249853 19.757141 64.248394 19.757964 64.248237 19.758768 64.247703 19.758588 64.246889 19.760434 64.245503 19.761887 64.244577 19.761238 64.242706 19.762313 64.242236 19.756465 64.241925 19.756317 64.24126 19.757667 64.240673 19.757789 64.239898 19.759846 64.239283 19.759345 64.238282 19.759822 64.237742 19.761499 64.236079 19.763222 64.235788 19.765657 64.235475 19.765612 64.234675 19.768594 64.234812 19.770162 64.233988 19.772417 64.233814 19.773837 64.234057 19.774801 64.233439 19.776053 64.232419 19.775597 64.232483 19.774884 64.232178 19.774531 64.231798 19.772 64.231281 19.771203 64.231001 19.768274 64.230699 19.767818 64.229289 19.768441 64.228624 19.76814 64.228249 19.767054 64.227916 19.767729 64.228162 19.77024 64.227245 19.772585 64.227771 19.774724 64.227659 19.775533 64.22437 19.767633 64.220869 19.764244 64.220723 19.762985 64.221062 19.762105 64.221207 19.760063 64.220345 19.758702 64.220188 19.751253 64.218554 19.746894 64.218903 19.745603 64.218355 19.744288 64.217214 19.7433 64.216694 19.744258 64.216207 19.743982 64.215687 19.744939 64.215242 19.744773 64.215692 19.743084 64.21676 19.741792 64.218614 19.741334 64.219545 19.738475 64.22113 19.736328 64.221677 19.734342 64.222225 19.734008 64.22287 19.730076 64.223589 19.730075 64.224274 19.731307 64.225322 19.729083 64.226033 19.72939 64.226158 19.728067 64.226756 19.727532 64.22721 19.729041 64.228673 19.731415 64.228056 19.735971 64.228155 19.738977 64.228569 19.740274 64.228343 19.743646 64.229026 19.744982 64.229464 19.742052 64.231128 19.741979 64.231548 19.743071 64.231277 19.744787 64.231594 19.74803 64.23137 19.74965 64.233957 19.748677 64.234233 19.746756 64.233612 19.74481 64.233478 19.743139 64.234607 19.742887 64.235178 19.74173 64.235054 19.739649 64.235616 19.7388 64.23602 19.735451 64.237499 19.733907 64.237504 19.730399 64.23807 19.726041 64.237768 19.725585 64.237849 19.724255 64.23817 19.723991 64.238265 19.722147 64.237996 19.722108 64.237752 19.719494 64.238107 19.719647 64.238722 19.718496 64.239465 19.715917 64.239363 19.714664 64.238614 19.714145 64.238781 19.712931 64.239371 19.712704 64.239921 19.710614 64.241025 19.709635 64.241773 19.70685 64.242302 19.707235 64.242453 19.708288 64.243388 19.708627 64.243433 19.710285 64.244549 19.710546 64.246134 19.708395 64.246507 19.706177 64.246395 19.705335 64.247105 19.703989 64.246793 19.70219 64.247693 19.700459 64.248002 19.697302 64.248736 19.69503 64.247922 19.694505 64.247334 19.689457 64.251971 19.68485 64.25223 19.683544 64.253617 19.682086 64.254374 19.682296 64.254904 19.684332 64.255334 19.68336 64.256543 19.68353 64.257535 19.686767 64.258195 19.687273 64.258849 19.686332 64.260703 19.687523 64.261394 19.686897 64.261671 19.688278 64.262376 19.688791 64.262291 19.690328 64.261514 19.692491 64.262823 19.692262 64.262941 19.692899 64.262912 19.695684 64.263299 19.698011 64.26316 19.699851 64.265301 19.697053 64.266901 19.69263 64.268094 19.691661 64.26949 19.693201 64.269754 19.695098 64.27049 19.696132 64.271894 19.695709 64.272635 19.696537 64.273172 19.694959 64.274099 19.69385 64.274224 19.695934 64.273522 19.696972 64.275356 19.700641 64.276009 19.70311 64.275889 19.70423 64.275506 19.705107 64.274566 19.704974 64.2745 19.705791 64.273401 19.706566 64.272496 19.708505"
            },
            "name":"Åhedbäcken"
        }
    ],
    "temporalCoverage":"2008-04-23T20:00:00Z/2017-10-31T14:00:00Z",
    "url":"https://meta.fieldsites.se/objects/kyCDtIXhWr-xJcyah0_hOyBt",
    "variableMeasured":[
        {
            "@type":"PropertyValue",
            "description":"Time instant",
            "name":"TIMESTAMP",
            "unitText":null
        },
        {
            "@type":"PropertyValue",
            "description":"Discharge",
            "name":"Q",
            "unitText":"m3 s-1"
        }
    ]
    }
    ```


    
## References

- [Shema.org/Dataset](https://schema.org/Dataset)
- [Schema.org validator](https://validator.schema.org)
- [Google Dataset structured data](https://developers.google.com/search/docs/appearance/structured-data/dataset)