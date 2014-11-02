Whitelist-Validation
====================

Input validation to help prevent XSS when rich text editors are needed. All credit to eksith (http://eksith.wordpress.com/2011/06/14/whitelist-santize-htmlagilitypack/). Minor updates make it work with latest versions of .NET and HtmlAgilityPack. 

Encoding untrusted data according to the appropriate context is the end all, be all of XSS protection. However, some use cases requires users to submit stylizations via HTML tags. In this case, a whitelist should be created to filter out unwanted tags and attributes (such as eventhandlers). Class is a singleton and thread safe. Modify the ValidHtmlTags dictionary to fit your needs. 

```
HtmlUtility.SanitizeHtml(string untrustedData);
```

Requires: HtmlAgilityPack
