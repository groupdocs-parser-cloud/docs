---
id: "extract-text"
url: "parser/extract-text"
title: "Extract Text"
productName: "GroupDocs.Parser Cloud"
weight: 2
description: ""
keywords: ""
---






# Introduction #

This REST API provides the functionality to extract text from the document.
There are several ways to extract text from a document:

* Extract only text;
* Extract formatted text by setting pages extraction mode option;
* Extract text from specific pages by setting the pages range.

For protected documents, it is also required to provide a password.
The table below contains the full list of properties that can be specified when extracting text from a document.


 

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage.|Required.
|FileInfo.StorageName|Storage name|It could be omitted for default storage.
|FileInfo.Password|The password to open file|It should be specified only for password-protected documents.
|ContainerItemInfo.RelativePath|The relative path of the container.|Should be specified only for container files like ZIP archives, emails or PDF portfolios.
|ContainerItemInfo.Password|Password for processing password-protected container items.|It should be specified only for password-protected container items.
|FormattedTextOptions.Mode|The formatted text extraction mode. |Possible values are: “PlainText”, “Html”, “Markdown”.
|StartPageNumber|Extraction start page.|The zero-based index. Extracts all pages if not specified.
|CountPagesToExtract|The number of pages to extract.|Required if StartPageNumber is specified.


## Resource URI ##



 

```html 

HTTP POST ~/text

 ```

 


[Swagger UI](https://apireference.groupdocs.cloud/parser/#/Parse/Text) lets you call this REST API directly from the browser.  
|---|---

## Use Cases ##





