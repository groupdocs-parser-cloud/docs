---
id: "extract-images"
url: "parser/extract-images"
title: "Extract Images"
productName: "GroupDocs.Parser Cloud"
weight: 3
description: ""
keywords: ""
---






## Introduction ##

This REST API provides the functionality to extract images from the document. There are following ways to extract images from a document:

* Extract all images from the whole document;
* Extract images from specific document pages by setting pages range.

It saves extracted images to the storage so they can be easily downloaded. The API allows extracting images from containers like ZIP archives, PDF portfolios, Email attachments, MS Outlook storages (PST/OST). For protected documents, it is also required to provide a password.

The table below contains the full list of properties that can be specified when extracting images from a document.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage. |Required.
|FileInfo.StorageName|Storage name|It could be omitted for default storage.
|FileInfo.Password|The password to open file|It should be specified only for password-protected documents.
|ContainerItemInfo.RelativePath|The relative path of the container.|Should be specified only for container files like ZIP archives, emails or PDF portfolios.
|ContainerItemInfo.Password|Password for processing password-protected container items.|It should be specified only for password-protected container items.
|StartPageNumber|Extraction start page.|The zero-based index.Extracts from the whole document if not specified.
|CountPagesToExtract|The number of pages to extract.|Required if StartPageNumber is specified.

### Resource URI ###

```html
HTTP POST ~/images
```

[Swagger UI](https://apireference.groupdocs.cloud/parser/#/Parse/Images) lets you call this REST API directly from the browser.  

### Use Cases ###
