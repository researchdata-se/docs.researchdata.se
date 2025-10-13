# XML sitemap (sitemap.xml)

The repository `sitemap.xml` should list all the URL:s for the latest version of each dataset in the catalogue:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9" xsi="http://www.w3.org/2001/XMLSchema-instance" schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9 http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd">
  <url>
    <loc>https://example.org/catalogue/dataset/ds-1</loc>
  </url>
  <url>
    <loc>https://example.org/catalogue/dataset/ds-2</loc>
  </url>
</urlset>
```

__Example sitemap.xml__

* [fieldsites.se](https://meta.fieldsites.se/sitemap.xml)
* [Researchdata.se catalogue](https://researchdata.se/en/sitemap.xml)

More information about sitemap.xml can be found on the official webpage: [sitemaps.org](https://www.sitemaps.org)

 The resource metadata should be available as [Schema.org JSON-LD](../metadata/schema-org-json-ld.md) on the landing page of each dataset.

## robots.txt

The repository should implement a sitemap.xml endpoint. This will make it possible for web crawlers to find and index the landing page for each dataset. The URL pointing to sitemap.xml should be added to `robots.txt`, for example:

```markdown
# robots.txt
#
# This file is to prevent the crawling and indexing of certain parts
# of your site by web crawlers and spiders run by sites like Yahoo!
# and Google. By telling these "robots" where not to go on your site,
# you save bandwidth and server resources.
#
# For more information about the robots.txt standard, see:
# http://www.robotstxt.org/robotstxt.html

Sitemap: https://example.org/catalogue/sitemap.xml
Crawl-delay: 10
```

## References
- [https://www.sitemaps.org/protocol.html](https://www.sitemaps.org/protocol.html)