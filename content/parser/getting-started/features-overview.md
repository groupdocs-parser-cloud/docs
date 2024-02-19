---
id: "features-overview"
url: "parser/features-overview"
title: "Features Overview"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

GroupDocs.Parser Cloud is a document data extraction REST API from over 50 document types. One of the most valuable features of GroupDocs.Parser Cloud is parsing documents with predefined templates. It's easy to define template and extract data from invoices, prices or other kinds of your typical documents. The API also provides methods to extract images, extract text. You can do it with regular documents and containers like ZIP archives, OST/PST mail data files and PDF portfolios. Below, the shortlist of possible actions:

## Parse Document by Template

GroupDocs.Parser Cloud allows parsing documents by user-defined templates. It is easy to create a template with data field definitions, table definitions. Then it's easy to use the template and extract data such as text fields, numbers, tables from your typical documents.

The template can be passed as an object. Also, you can save your named templates in the storage and parse your documents with them.\\

## Extract Text

GroupDocs.Parser Cloud provides text extraction method that covers various text retrieval scenarios:

* Extract a plain text from any of the supporting documents;
* Extract HTML or Markdown-formatted text for a fast preview;
* Extract particular pages of plain or formatted text.

### Extract Formatted Text

In addition to standard text extraction modes, GroupDocs.Parser Cloud API provides an option to extract a formatted text for those cases when simple plain text is not enough and you may need to keep formatting like text style, table layout, etc.

At this moment the following formats are supported:

* Plain Text
* Markdown
* HTML

#### Plain Text

With Plain Text mode GroupDocs.Parser Cloud performs formatting in plain text making extracted text look closer to the original. This is achieved due to special text positioning, box-drawing characters, etc.

#### Markdown

This mode is useful when you need to export the extracted text to any system that supports [Markdown](https://en.wikipedia.org/wiki/Markdown)-formatted text.

At this moment the following formattings are supported:

* Bold text
* Italic text
* Hyperlinks
* Headings
* Numbering and bullets lists
* Tables

#### HTML

GroupDocs.Parser Cloud also supports HTML formatting.

Following HTML tags are now supported when extracting text with this formatting mode:

|Tag|Description|
|---|---|
|\<p\>|Paragraph is surrounded by \<p\> tag|
|\<a\>|Hyperlinks|
|\<b\>|Text with Bold font is surrounded by \<b\> tag|
|\<i\>|Text with Italic font is surrounded by \<i\> tag|
|\<h1\> – \<h6\>|If the heading has 'Heading X' style, it's surrounded by \<hx\> tag|
|\<ol\>/\<ul\>|Numbering and bullets lists|
|\<table\>|Tables|

## Extract Images

GroupDocs.Parser Cloud supports Images extraction from documents. You may call this method and retrieve all document images and save them.

## Document information extraction

GroupDocs.Parser Cloud allows obtaining basic information about source document - file type, size, pages count. The API also provides a method to extract information about container items such as Zip archives, emails with attachments, Ost files or Pdf Portfolio.

## Template Management

GroupDocs.Parser Cloud provides methods that help you to create, update, retrieve and delete user-generated template files that are used in Parse by Document Template functionality.

# API Endpoint Groups Overview #

|Endpoint Group|Description
|---|---
|Info|It contains endpoints for obtaining list of formats supported by GroupDocs.Parser Cloud, getting basic information about the document and its pages, getting information about container items.
|Parse|Contains endpoints for Parse by template, Text and Images extraction functionality
|Template|Contains endpoints for managing user-generated template files
|File|Contains endpoints for upload, download, copy, move, delete files in the storage
|Folder|Contains endpoints for creating, copy, move, delete folders in the storage
|Storage|Contains endpoints for obtaining storage information and file information

# Security and Authentication #

The GroupDocs.Parser Cloud API is secured and requires authentication. Two keys Client Id and Client Secret are required for Authentication which can be created at the [Dashboard](http://dashboard.groupdocs.cloud).
Check [Authenticating API Requests]({{< ref "total/overview-rest-api/authenticating-api-requests.md" >}}) article for complete example.

# SDK examples #

Check out our GitHub [repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser SDKs along with working examples, to get you started in no time. 

At the moment following SDKs are provided: 

* .NET 2.0 ([Sources](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-dotnet), NuGet Package)
* Java ([Sources](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-java), Jar)

# API Explorer #

The easiest way to try out our API right away in your browser! With the [GroupDocs Cloud API explorer](https://apireference.groupdocs.cloud/parser/). This is a collection of Swagger documentation for the GroupDocs Cloud APIs. You can get information about all the resources in the API. It also provides testing and interactivity to our API endpoint documentation.
