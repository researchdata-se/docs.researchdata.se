# Controlled vocabularies
Controlled vocabularies for metadata play a crucial role in systematically organising and managing information, particularly in the context of datasets.
A controlled vocabulary consists of predefined terms with assigned meanings, ensuring consistency when describing and categorizing information.

In addition, persistent identifiers (PIDs) are used to provide robust links and avoid disambiguation when referring to definitions of individuals, organisations or places, and may also be used in a similar manner.

A selection of best practices regarding controlled vocabularies and persistent identifiers are listed below. These will make it more likely that Researchdata.se will be able to reuse the metadata when harvesting from a data source. 

## Organisations

For organisations, providing a [ROR ID](https://ror.org) PID is the preferred method for identifying the organisation.

Examples:  
`https://ror.org/05ynxx418`  
`https://ror.org/040wg7k59`  
`https://ror.org/03zttf063`

## Persons

To identify a person, use [ORCID](https://orcid.org), a PID for researchers and other contributors.  

Examples:  
`https://orcid.org/0000-0002-9227-8514`

[Structure of the ORCID Identifier](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier)

## Subjects & keywords

There are multiple vocabularies used to categorise and tag resources. Some of them cover several disciplines, while others are specific to a limited set of research domains.

### AAT – The Art & Architecture Thesaurus  
[https://www.getty.edu/research/tools/vocabularies/aat/](https://www.getty.edu/research/tools/vocabularies/aat/)  
     
Example term:  
[http://vocab.getty.edu/page/aat/300191918](http://vocab.getty.edu/page/aat/300191918)

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="AAT The art & Architecture Thesaurus" 
            schemeURI="http://vocab.getty.edu/page/aat/" 
            valueURI="http://vocab.getty.edu/page/aat/300191918"
            classificationCode="300191918" 
            xml:lang="en">Asian coins</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://vocab.getty.edu/page/aat/300191918",
                    "inDefinedTermSet": "http://vocab.getty.edu/page/aat/",
                    "termCode": "300191918",
                    "name": "Asian coins"
                }
            ]
        }
        ```

### AGROVOC – Vocabulary for Agricultural Sciences 
[https://agrovoc.fao.org/browse/agrovoc](https://agrovoc.fao.org/browse/agrovoc)  
     
Example term:  
[http://aims.fao.org/aos/agrovoc/c_2536](http://aims.fao.org/aos/agrovoc/c_2536)  

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="AGROVOC Vocabulary for Agricultural Sciences" 
            schemeURI="http://aims.fao.org/aos/agrovoc" 
            valueURI="http://aims.fao.org/aos/agrovoc/c_2152"
            classificationCode="c_2536" 
            xml:lang="en">elks</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://aims.fao.org/aos/agrovoc/c_2536",
                    "inDefinedTermSet": "https://agrovoc.fao.org/browse/agrovoc",
                    "termCode": "c_2536",
                    "name": "elks"
                }
            ]
        }
        ```

### ALLFO – Allmän finländsk ontologi 
[https://finto.fi/yso](https://finto.fi/yso)  
     
Example term:  
[http://www.yso.fi/onto/yso/p13693](http://www.yso.fi/onto/yso/p13693)  


??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="ALLFO - Allmän finländsk ontologi" 
            schemeURI="https://finto.fi/yso" 
            valueURI="http://www.yso.fi/onto/yso/p13693"
            classificationCode="p13693" 
            xml:lang="en">elk</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://www.yso.fi/onto/yso/p13693",
                    "inDefinedTermSet": "https://finto.fi/yso",
                    "termCode": "p13693",
                    "name": "elk"
                }
            ]
        }
        ```

### ELSST – The European Language Social Science Thesaurus 
[https://elsst.cessda.eu](https://elsst.cessda.eu)  
     
Example term:  
[https://elsst.cessda.eu/id/4/a74cd285-d1c6-4e55-8c0d-faf0fe94399f](https://elsst.cessda.eu/id/4/a74cd285-d1c6-4e55-8c0d-faf0fe94399f) 

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="ELSST The European Language Social Science Thesaurus" 
            schemeURI="https://elsst.cessda.eu" 
            valueURI="https://elsst.cessda.eu/id/4/a74cd285-d1c6-4e55-8c0d-faf0fe94399f"
            classificationCode="urn:ddi:int.cessda.elsst:a74cd285-d1c6-4e55-8c0d-faf0fe94399f:4" 
            xml:lang="en">ENVIRONMENT</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "https://elsst.cessda.eu/id/4/a74cd285-d1c6-4e55-8c0d-faf0fe94399f",
                    "inDefinedTermSet": "https://elsst.cessda.eu",
                    "termCode": "urn:ddi:int.cessda.elsst:a74cd285-d1c6-4e55-8c0d-faf0fe94399f:4",
                    "name": "ENVIRONMENT"
                }
            ]
        }
        ```


### EnvThes – Environmental Thesaurus
[https://vocabs.lter-europe.net/envthes](https://vocabs.lter-europe.net/envthes)  

Example term:  
[http://vocabs.lter-europe.net/EnvThes/20800](http://vocabs.lter-europe.net/EnvThes/20800)  

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="EnvThes Environmental Thesaurus" 
            schemeURI="https://vocabs.lter-europe.net/envthes" 
            valueURI="http://vocabs.lter-europe.net/EnvThes/20800"
            classificationCode="20800" 
            xml:lang="en">aluminum</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://vocabs.lter-europe.net/EnvThes/20800",
                    "inDefinedTermSet": "https://vocabs.lter-europe.net/envthes",
                    "termCode": "20800",
                    "name": "aluminum"
                }
            ]
        }
        ```

### FISH Thesaurus of Monument Types
[https://collectionstrust.org.uk/resource/thesaurus-of-monument-types-fish](https://collectionstrust.org.uk/resource/thesaurus-of-monument-types-fish)   

Example term:  
[http://purl.org/heritagedata/schemes/560/concepts/142104](http://purl.org/heritagedata/schemes/560/concepts/142104)  

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="FISH Archaeological Sciences Thesaurus" 
            schemeURI="http://purl.org/heritagedata/schemes/560" 
            valueURI="http://purl.org/heritagedata/schemes/560/concepts/142104"
            classificationCode="142104" 
            xml:lang="en">Archaeomagnetism</subject>
        </subjects>
        ```
    === "JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://purl.org/heritagedata/schemes/560/concepts/142104",
                    "inDefinedTermSet": "http://purl.org/heritagedata/schemes/560",
                    "termCode": "142104",
                    "name": "Archaeomagnetism"
                }
            ]
        }
        ```

### GCMD Vocabulary for Earth Science
[https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords](https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords)  
     
Example term:  
[https://gcmd.earthdata.nasa.gov/kms/concept/b3b14df8-5197-4a26-ae61-882fdba706f3](https://gcmd.earthdata.nasa.gov/kms/concept/b3b14df8-5197-4a26-ae61-882fdba706f3) 

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="GCMD Vocabulary for Earth Science" 
            schemeURI="https://gcmd.earthdata.nasa.gov/kms/concepts/concept_scheme/sciencekeywords" 
            valueURI="https://gcmd.earthdata.nasa.gov/kms/concept/b3b14df8-5197-4a26-ae61-882fdba706f3"
            classificationCode="b3b14df8-5197-4a26-ae61-882fdba706f3" 
            xml:lang="en">FOOD STORAGE</subject>
        </subjects>
        ```
    === "JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "https://gcmd.earthdata.nasa.gov/kms/concept/b3b14df8-5197-4a26-ae61-882fdba706f3",
                    "inDefinedTermSet": "https://gcmd.earthdata.nasa.gov/kms/concepts/concept_scheme/sciencekeywords",
                    "termCode": "b3b14df8-5197-4a26-ae61-882fdba706f3",
                    "name": "FOOD STORAGE"
                }
            ]
        }
        ```

### GEMET – General Multilingual Environmental Thesaurus 
[http://www.eionet.europa.eu/gemet/](http://www.eionet.europa.eu/gemet) 

Example term:  
[http://www.eionet.europa.eu/gemet/concept/1500](http://www.eionet.europa.eu/gemet/concept/1500)  

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="GEMET General Multilingual Environmental Thesaurus" 
            schemeURI="http://www.eionet.europa.eu/gemet" 
            valueURI="http://www.eionet.europa.eu/gemet/concept/1500"
            classificationCode="1500" 
            xml:lang="en">coal</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://www.eionet.europa.eu/gemet/concept/1500",
                    "inDefinedTermSet": "http://www.eionet.europa.eu/gemet",
                    "termCode": "1500",
                    "name": "coal"
                }
            ]
        }
        ```

### ICD-10 – International Classification of Diseases 
[https://icd.who.int/browse10/2019/en](https://icd.who.int/browse10/2019/en)

Example term:  
[https://icd.who.int/browse10/2019/en#/I20-I25](https://icd.who.int/browse10/2019/en#/I20-I25)

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="ICD-10 International Classification of Diseases" 
            schemeURI="https://icd.who.int/browse10/2019/" 
            valueURI="https://icd.who.int/browse10/2019/en#/I20-I25"
            classificationCode="I20-I25" 
            xml:lang="en">Ischaemic heart diseases</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "https://icd.who.int/browse10/2019/en#/I20-I25",
                    "inDefinedTermSet": "https://icd.who.int/browse10/2019/",
                    "termCode": "I20-I25",
                    "name": "Ischaemic heart diseases"
                }
            ]
        }
        ```

### INSPIRE glossary
[https://inspire.ec.europa.eu/glossary](https://inspire.ec.europa.eu/glossary)

Example term:  
[http://inspire.ec.europa.eu/glossary/Aqueduct](http://inspire.ec.europa.eu/glossary/Aqueduct)

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="INSPIRE glossary" 
            schemeURI="http://inspire.ec.europa.eu/glossary" 
            valueURI="http://inspire.ec.europa.eu/glossary/Aqueduct"
            classificationCode="Aqueduct" 
            xml:lang="en">Aqueduct</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://inspire.ec.europa.eu/glossary",
                    "inDefinedTermSet": "http://inspire.ec.europa.eu/glossary/Aqueduct",
                    "termCode": "Aqueduct",
                    "name": "Aqueduct"
                }
            ]
        }
        ```

### LCSH – Library of Congress Subject Headings
[http://id.loc.gov/authorities/subjects/](http://id.loc.gov/authorities/subjects/)  
     
Example term:  
[https://id.loc.gov/authorities/subjects/sh2009009655](https://id.loc.gov/authorities/subjects/sh2009009655) 

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="Library of Congress Subject Headings (LCSH)" 
            schemeURI="https://id.loc.gov/authorities/subjects/" 
            valueURI="https://id.loc.gov/authorities/subjects/sh2009009655"
            classificationCode="sh2009009655" 
            xml:lang="en">Climate change mitigation</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "https://id.loc.gov/authorities/subjects/sh2009009655",
                    "inDefinedTermSet": "https://id.loc.gov/authorities/subjects/",
                    "termCode": "sh2009009655",
                    "name": "Climate change mitigation"
                }
            ]
        }
        ```

### MeSH – Medical Subject Headings 
[https://www.nlm.nih.gov/mesh](https://www.nlm.nih.gov/mesh)  
     
Example term:  
[http://id.nlm.nih.gov/mesh/D003069](http://id.nlm.nih.gov/mesh/D003069) 

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject 
            subjectScheme="MeSH Medical Subject Headings" 
            schemeURI="http://id.nlm.nih.gov/mesh" 
            valueURI="http://id.nlm.nih.gov/mesh/D003069"
            classificationCode="D003069" 
            xml:lang="en">Coffee</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "http://id.nlm.nih.gov/mesh/D003069",
                    "inDefinedTermSet": "http://id.nlm.nih.gov/mesh",
                    "termCode": "D003069",
                    "name": "Coffee"
                }
            ]
        }
        ```

### NASA Thesaurus / NASA STI Thesaurus 
[https://sti.nasa.gov/nasa-thesaurus](https://sti.nasa.gov/nasa-thesaurus)

### SSIF 2025 – Standard för svensk indelning av forskningsämnen 2025

[https://www.scb.se/dokumentation/klassifikationer-och-standarder/standard-for-svensk-indelning-av-forskningsamnen/](https://www.scb.se/dokumentation/klassifikationer-och-standarder/standard-for-svensk-indelning-av-forskningsamnen/)  


??? example "Example usage"
    === "DataCite XML"
        ```xml
        <subjects>
            <subject
            subjectScheme="Standard för svensk indelning av forskningsämnen 2025"
            schemeURI="https://begrepp.uka.se/SSIF/"
            classificationCode="105"
            valueURI="https://begrepp.uka.se/SSIF/105"
            xml:lang="en">Earth and Related Environmental Sciences</subject>
        </subjects>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "keywords": [
                {
                    "@type": "DefinedTerm",
                    "@id": "https://begrepp.uka.se/SSIF/105",
                    "inDefinedTermSet": "https://begrepp.uka.se/SSIF/",
                    "termCode": "105",
                    "name": "Earth and Related Environmental Sciences"
                }
            ]
        }
        ```

## Geography

### Geonames
Commonly used identifier service for countries, regions, cities, and other places.

Examples:  
`https://sws.geonames.org/2661886/` - Sweden  
`https://sws.geonames.org/2699050/` - Kronoberg  
`https://sws.geonames.org/2701727/`- Karlshamn  

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <geoLocations>
            <geoLocation>
                <geoLocationPlace>Sweden</geoLocationPlace>
            </geoLocation>
        </geoLocations>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "spatialCoverage": {
                "@type": "Place",
                "@id": "https://sws.geonames.org/2661886/",
                "name": "Sweden",
                "identifier": "SE"
            }
        }
        ```



## Language

[Use ISO 639-3](https://en.wikipedia.org/wiki/ISO_639-3) language codes.  
Examples: eng, deu, swe  

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <language>eng</language>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "inLanguage": {
                "@type": "Language",
                "@id": "http://lexvo.org/id/iso639-3/swe",
                "name": "Swedish",
                "identifier": "swe"
            }
        }
        ```

## License

For recommendations on open licenses and marks in a Swedish context, see the following summary by Digg:  
[Rekommendation om öppna licenser och immaterialrätt](https://www.digg.se/kunskap-och-stod/oppna-och-delade-data/offentliga-aktorer/rekommendation-om-oppna-licenser-och-immaterialratt)

[SPDX License List](https://spdx.org/licenses/)

Examples:  
`https://creativecommons.org/publicdomain/zero/1.0/`  
`https://creativecommons.org/licenses/by/4.0/`

??? example "Example usage"
    === "DataCite XML"
        ```xml
        <rightsList>
            <rights 
            ml:lang="en" 
            schemeURI="https://spdx.org/licenses/" 
            rightsIdentifierScheme="SPDX" 
            rightsIdentifier="CC0-1.0" 
            rightsURI="https://creativecommons.org/publicdomain/zero/1.0/">
            Creative Commons Zero v1.0 Universal</rights>
        </rightsList>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "license": "https://creativecommons.org/publicdomain/zero/1.0/"
        }
        ```

## Dataset type

To mark a specific type of dataset, the EU Vocabulary [Dataset Type](https://op.europa.eu/en/web/eu-vocabularies/concept-scheme/-/resource?uri=http://publications.europa.eu/resource/authority/dataset-type) provides a way to classify a dataset as syntetic data, test data etc.

A good use case for providing a dataset type is to mark syntetic datasets.

??? example "Example for syntetic data"
    === "DataCite XML"
        ```xml
        <resourceType resourceTypeGeneral="Dataset">SYNTHETIC_DATA</resourceType>
        ```
    === "Schema.org JSON-LD"
        ```json
        {
            "@context":"https://schema.org/",
            "@type": "Dataset",
            "additionalType": "http://publications.europa.eu/resource/authority/dataset-type/SYNTHETIC_DATA"
        }
        ```
