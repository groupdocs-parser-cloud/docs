---
id: "parse-by-template"
url: "parser/parse-by-template"
title: "Parse by Template"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API provides the functionality to extract data from documents. This method parses document content by a user-generated template.

The template can be provided as an object or storage path. For protected documents, it is also required to provide a password.

The table below contains the full list of properties that can be specified when parsing documents by a template.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage. |Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.
|FileInfo.Password|The password to open file|It should be specified only for password-protected documents.
|ContainerItemInfo.RelativePath|The relative path of the container.|Should be specified only for container files like ZIP archives, emails or PDF portfolios.
|ContainerItemInfo.Password|Password for processing password-protected container items.|It should be specified only for password-protected container items.
|TemplatePath|The path of the file, located in the storage, which contains a user-generated template to parse data. It is used when the template parameter is not provided. |The template must be provided by this field or by Template.
|Template|User-generated [template](#template) object to extract metadata from the document. |Template must be provided by this field or by TemplatePath.

## Template

|Name|Description|Comment
|---|---|---
|Template.Fields|Template fields.|Required if Template. Tables are not provided.
|Field.FieldName|A unique template field name.|Required.
|Field.PageIndex|The page index.|An integer value that represents the index of the page where the template item is located; null if the template item is located on any page.
|FieldPosition. FieldPositionType|Provides a template field position.|Possible values are: “Fixed”, “Linked”, “Regex”. Required.
|FieldPosition.Rectangle|[A rectangular area](#rectangle) on the page that bounds the field value.|Required if “Fixed” FieldPositionType is set.
|FieldPosition.Regex|String expression to find a field value by a regular expression.|Required if “Regex” FieldPositionType is set.
|FieldPosition.MatchCase|The value that indicates whether a text case isn't ignored.|Is used if Regex parameter is set.
|FieldPosition.LinkedFieldName|The name of the linked field.|Required if “Linked” FieldPositionType is set.
|FieldPosition.IsLeftLinked|The value that indicates whether a field is searched by the left from the linked field.|Is used if “Linked” FieldPositionType is set.
|FieldPosition.IsRightLinked|The value that indicates whether a field is searched by the right from the linked field.|Is used if “Linked” FieldPositionType is set.
|FieldPosition.IsTopLinked|The value that indicates whether a field is searched by the top from the linked field.|Is used if “Linked” FieldPositionType is set.
|FieldPosition.IsBottomLinked|The value that indicates whether a field is searched by the bottom from the linked field.|Is used if “Linked” FieldPositionType is set.
|FieldPosition.SearchArea|The size of the area where a field is searched.|Required if “Linked” FieldPositionType is set.
|SearchArea.Height|The height of search area.|
|SearchArea.Width|The width of search area.|
|FieldPosition.AutoScale|The value that indicates whether SearchArea is scaled by the linked field size.|Is used if “Linked” FieldPositionType is set.
|Template.Tables|Template tables.|Required if Template.Fields are not provided.
|Table.FieldName|A unique template table name.|Required.
|Table.PageIndex|The page index.|An integer value that represents the index of the page where the template item is located; null if the template item is located on any page.
|Table.DetectorParametes|Provides parameters for the table detection algorithms.|Required if TableLayout is not provided.
|DetectorParameters.MinRowCount|The minimum number of the table rows.|
|DetectorParameters.MinColumnCount|The minimum number of the table columns.|
|DetectorParameters.MinVerticalSpace|The minimum space between the table columns.|
|DetectorParameters.HasMergedCells|The value that indicates whether the table has merged cells.|
|DetectorParameters.Rectangle|The [rectangular area](#rectangle) that contains the table.|
|DetectorParameters.VerticalSeparators|The table columns separators.|
|Table.TableLayout|Provides the template table layout which is used Table to define table position.|Required if DetectorParameters is not provided.
|TableLayout.VerticalSeparators|The table columns separators.|
|TableLayout.HorizontalSeparators|The table rows separators.|

## Rectangle

|Name|Description|Comment
|---|---|---
|Rectangle.Position|The coordinates of the upper-left corner of the rectangular area.|Required if Rectangle.Coordinates is not provided.
|Position.X|X-coordinate of upper-left rectangle corner.|
|Position.Y|Y-coordinate of upper-left rectangle corner.|
|Rectangle.Size|Represents a size of rectangular area.|Required if Rectangle.Coordinates is not provided.
|Size.Height|The height of rectangular area.|
|Size.Width|The width of rectangular area.|
|Rectangle.Coordinates|Coordinates of the rectangular area edges.|
|Coordinates.Top|The y-coordinate of the top edge of the rectangular area.|
|Coordinates.Right|The x-coordinate of the right edge of the rectangular area.|
|Coordinates.Left|The x-coordinate of the left edge of the rectangular area.|
|Coordinates.Bottom|The y-coordinate of the bottom edge of the rectangular area.|

## Resource URI

```html
HTTP POST ~/parse
```

[Swagger UI](https://apireference.groupdocs.cloud/parser/#/Parse/Parse) lets you call this REST API directly from the browser.  

## Use Cases
