---
id: "groupdocs-parser-for-cloud-19-11-release-notes"
url: "parser/groupdocs-parser-for-cloud-19-11-release-notes"
title: "GroupDocs.Parser for Cloud 19.11 Release Notes"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
---

{{< alert style="info" >}}
This page contains release notes for GroupDocs.Parser Cloud 19.11
{{< /alert >}}

## Overview ##

GroupDocs.Parser Cloud is a document data extraction REST API from over 50 document types. One of the most valuable features of GroupDocs.Parser Cloud is parsing documents with predefined templates. It's easy to define template and extract data from invoices, prices or other kinds of your typical documents. The API also provides methods to extract images, extract text. You can do it with regular documents and containers like ZIP archives, OST/PST mail data files and PDF portfolios.

### Major Features ###

Below are the shortlist of possible actions / features availavle in GroupDocs.Parser Cloud API:

#### Parse Document by Template ####

GroupDocs.Parser Cloud allows parsing documents by user-defined templates. It is easy to create a template with data field definitions, table definitions. Then it's easy to use the template and extract data such as text fields, numbers, tables from your typical documents. The template can be passed as an object. Also, you can save your named templates in the storage and parse your documents with them.

#### Extract Text ####

GroupDocs.Parser Cloud provides text extraction method that covers various text retrieval scenarios:

* Extract a plain text from any of the supporting documents;
* Extract HTML or Markdown-formatted text for a fast preview;
* Extract particular pages of plain or formatted text.

#### Extract Formatted Text ####

In addition to standard text extraction modes, GroupDocs.Parser Cloud API provides an option to extract a formatted text for those cases when simple plain text is not enough and you may need to keep formatting like text style, table layout, etc. At this moment the following formats are supported:

* Plain Text
* Markdown
* HTML

#### Extract Images ####

GroupDocs.Parser Cloud supports Images extraction from documents. You may call this method and retrieve all document images and save them.

#### Document information extraction ####

GroupDocs.Parser Cloud allows obtaining basic information about source document - file type, size, pages count. The API also provides a method to extract information about container items such as Zip archives, emails with attachments, Ost files or Pdf Portfolio.

#### Template Management ####

GroupDocs.Parser Cloud provides methods that help you to create, update, retrieve and delete user-generated template files that are used in Parse by Document Template functionality.

### API Endpoint Groups Overview ###

|Endpoint Group|Description
|---|---
|Info|It contains endpoints for obtaining a list of formats supported by GroupDocs.Parser Cloud, getting basic information about the document and its pages, getting information about container items.
|Parse|Contains endpoints for Parse by template, Text and Images extraction functionality
|Template|Contains endpoints for managing user-generated template files
|File|Contains endpoints for upload, download, copy, move, delete files in the storage
|Folder|Contains endpoints for creating, copy, move, delete folders in the storage
|Storage|Contains endpoints for obtaining storage information and file information

### Public API Examples ###

* [GroupDocs Parser Cloud API examples and documentation]({{< ref "parser/_index.md" >}})
