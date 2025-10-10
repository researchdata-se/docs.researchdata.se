# Landing page metadata

To make the metadata as machine-readable as possible, the metadata should be exposed in a structured format like Schema.org JSON-LD, which is a widely used standard for representing structured data on the web.

This will allow search engines and other applications to easily interpret and index the metadata, improving discoverability and accessibility.

There are also some additional ways for providing the metadata on the landing page: using HTML meta tags and HTTP headers.

## HTML meta tags
The metadata may be embedded in the HTML source of the landing page using `<meta>` and `<link>` tags. This is a common practice for search engine optimization (SEO) and can help improving the visibility of the dataset in search results.

### Example
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta name="description" content="The description of the dataset">
        <meta name="keywords" content="keyword1, keyword2, keyword3">
        <meta name="citation_title" content="Swedish political party programs and election manifestos">
        <meta name="citation_publisher" content="University of Gothenburg">
        <meta name="citation_publication_date" content="2024-05-30T14:25:55.848643Z">
        <meta name="citation_doi" content="10.5878/kcsf-k293">
        <link rel="type" href="https://schema.org/Dataset">
        <link rel="type" href="https://schema.org/AboutPage">
        <link rel="cite-as" href="https://doi.org/10.5878/kcsf-k293">
        <link rel="author" href="https://orcid.org/0000-0002-7365-0691">
        <link rel="describedby" type="application/ld+json" href="https://example.com/dataset/1/export/json_ld">
        <link rel="describedby" type="application/rdf+xml" href="https://example.com/dataset/1/export/dcat">
        <link rel="describedby" type="application/vnd.datacite.datacite+xml" href="https://example.com/dataset/1/export/datacite">
        <link rel="describedby" type="application/vnd.citationstyles.csl+json" href="https://example.com/dataset/1/export/csl">
        <link rel="item" href="https://example.com/dataset/1/files/data.csv">
        <link rel="item" href="https://example.com/dataset/1/files/readme.txt">
        <link rel="license" href="https://creativecommons.org/publicdomain/mark/1.0/">
        <script type="application/ld+json">{ ... }</script>
    </head>
    <body>
        ...
    </body>
</html>
```
A list of the basic set of meta links can be found in the FAIR Signposting Profile: [https://signposting.org/FAIR/#level1](https://signposting.org/FAIR/#level1)

## HTTP headers
The metadata links may also be included in the HTTP headers of the landing page. This is a useful, but less common practice. It is especially useful for certain applications or services that mainly rely on HTTP headers for metadata.

Including metadata links in the HTTP headers will allow applications to discover the metadata without having to parse the HTML of the landing page itself.

### Example
```
curl --head https://researchdata.se/en/catalogue/dataset/2024-640

HTTP/1.1 200 OK
server: nginx/1.27.4
date: Wed, 07 May 2025 07:43:13 GMT
content-type: text/html;charset=utf-8
link: <https://schema.org/Dataset>; rel="type", <https://schema.org/AboutPage>; rel="type", <https://researchdata.se/catalogue/dataset/2024-640/1/export/json_ld>; rel="describedby"; type="application/ld+json", <https://researchdata.se/catalogue/dataset/2024-640/1/export/dcat>; rel="describedby"; type="application/rdf+xml", <https://researchdata.se/catalogue/dataset/2024-640/1/export/datacite>; rel="describedby"; type="application/vnd.datacite.datacite+xml", <https://researchdata.se/catalogue/dataset/2024-640/1/export/csl>; rel="describedby"; type="application/vnd.citationstyles.csl+json", <https://orcid.org/0009-0007-2583-780X>; rel="author", <https://orcid.org/0000-0002-5544-7147>; rel="author", <https://creativecommons.org/licenses/by/4.0/>; rel="license", <https://doi.org/10.5878/1yx0-hx90>; rel="cite-as"

```




## References
- [Schema.org](https://schema.org/)
- [Signposting - FAIR profile](https://signposting.org/FAIR/)