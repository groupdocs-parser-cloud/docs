---
id: "create-or-update-template"
url: "parser/create-or-update-template"
title: "Create or Update Template"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
---






# Introduction #

This REST API provides the functionality to save or update files that can be used in Parse endpoint. It's easy to define and save the template to extract data from invoices, prices or other kinds of your typical documents.

The table below contains the full list of properties.


 

|Name|Description|Comment
|---|---|---
|TemplatePath|The path of the template, located in the storage.|**Required.**
|FileInfo.StorageName|Storage name|It could be omitted for default storage.
|Template|User-generated template to extract metadata from the document.|Required.


### Template ###

{{id name#"TemplateParametersTable"/}}

|Name|Description|Comment
|---|---|---
|Template.Fields|Template fields.|Required if Template. Tables are not provided.
|Field.FieldName|A unique template field name.|Required.
|Field.PageIndex|The page index.|An integer value that represents the index of the page where the template item is located; null if the template item is located on any page.
|FieldPosition. FieldPositionType|Provides a template field position.|Possible values are: “Fixed”, “Linked”, “Regex”. Required.
|FieldPosition.Rectangle|A rectangular area on the page that bounds the field value.|Required if “Fixed” FieldPositionType is set.
|FieldPosition.Regex|String expression to find a field value by a regular expression.|Required if “Regex” FieldPositionType is set.
|FieldPosition.MatchCase|The value that indicates whether a test case isn't ignored.|It is used if the Regex parameter is set.
|FieldPosition.LinkedFieldName|The name of the linked field.|Required if “Linked” FieldPositionType is set.
|FieldPosition.IsLeftLinked|The value that indicates whether a field is searched by the left from the linked field.|It is used if “Linked” FieldPositionType is set.
|FieldPosition.IsRightLinked|The value that indicates whether a field is searched by the right from the linked field.|It is used if “Linked” FieldPositionType is set.
|FieldPosition.IsTopLinked|The value that indicates whether a field is searched by the top from the linked field.|It is used if “Linked” FieldPositionType is set.
|FieldPosition.IsBottomLinked|The value that indicates whether a field is searched by the bottom from the linked field.|It is used if “Linked” FieldPositionType is set.
|FieldPosition.SearchArea|The size of the area where a field is searched.|Required if “Linked” FieldPositionType is set.
|SearchArea.Height|The height of the search area.| 
|SearchArea.Width|The width of the search area.| 
|FieldPosition.AutoScale|The value that indicates whether SearchArea is scaled by the linked field size.|It is used if “Linked” FieldPositionType is set.
|Template.Tables|Template tables.|Required if Template. Fields are not provided.
|Table.FieldName|A unique template table name.|Required.
|Table.PageIndex|The page index.|An integer value that represents the index of the page where the template item is located; null if the template item is located on any page.
|Table.DetectorParametes|It provides parameters for the table detection algorithms.|Required if TableLayout is not provided.
|DetectorParameters.MinRowCount|The minimum number of table rows.| 
|DetectorParameters.MinColumnCount|The minimum number of table columns.| 
|DetectorParameters.MinVerticalSpace|The minimum space between the table columns.| 
|DetectorParameters.HasMergedCells|The value that indicates whether the table has merged cells.| 
|DetectorParameters.Rectangle|The rectangular area that contains the table.| 
|DetectorParameters.VerticalSeparators|The table columns separators.| 
|Table.TableLayout|Provides the template table layout which is used Table to define table position.|Required if DetectorParameters is not provided.
|TableLayout.VerticalSeparators|The table columns separators.| 
|TableLayout.HorizontalSeparators|The table rows separators.| 


### Rectangle ###

{{id name#"RectangleParametersTable"/}}

|Name|Description|Comment
|---|---|---
|Rectangle.Position|The coordinates of the upper-left corner of the rectangular area.|Required if Rectangle. Coordinates are not provided.
|Position.X|X-coordinate of upper-left rectangle corner.| 
|Position.Y|Y-coordinate of upper-left rectangle corner.| 
|Rectangle.Size|Represents the size of rectangular area.|Required if Rectangle. Coordinates are not provided.
|Size.Height|The height of the rectangular area.| 
|Size.Width|The width of the rectangular area.| 
|Rectangle.Coordinates|Coordinates of the rectangular area edges.| 
|Coordinates.Top|The y-coordinate of the top edge of the rectangular area.| 
|Coordinates.Right|The x-coordinate of the right edge of the rectangular area.| 
|Coordinates.Left|The x-coordinate of the left edge of the rectangular area.| 
|Coordinates.Bottom|The y-coordinate of the bottom edge of the rectangular area.| 


## Resource URI ##



 

```html 

HTTP PUT ~/template

 ```

 


[Swagger UI](https://apireference.groupdocs.cloud/parser/#/Template/CreateTemplate) lets you call this REST API directly from the browser. 
|---|---

## cURL Example ##

The following example demonstrates how to Create or Update Template.



 




 Request

```html 
* First get JSON Web Token
* Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&#x26;client_id#xxxx&#x26;client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
* cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/parser/template" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>" \
-d "{
    "Template": {
        "Fields": [
            {
                "FieldName": "Address",
                "FieldPosition": {
                    "FieldPositionType": "Fixed",
                    "Rectangle": {
                        "Position": {
                            "X": 13.0,
                            "Y": 35.0
                        },
                        "Size": {
                            "Height": 10.0,
                            "Width": 100.0
                        }
                    },
                    "MatchCase": false,
                    "IsLeftLinked": false,
                    "IsRightLinked": false,
                    "IsTopLinked": false,
                    "IsBottomLinked": false,
                    "AutoScale": false
                }
            },
            {
                "FieldName": "Company",
                "FieldPosition": {
                    "FieldPositionType": "Linked",
                    "MatchCase": false,
                    "LinkedFieldName": "Address",
                    "IsLeftLinked": false,
                    "IsRightLinked": false,
                    "IsTopLinked": false,
                    "IsBottomLinked": true,
                    "SearchArea": {
                        "Height": 15.0,
                        "Width": 100.0
                    },
                    "AutoScale": true
                }
            }
        ],
        "Tables": [
            {
                "TableName": "Totals",
                "DetectorParameters": {
                    "Rectangle": {
                        "Position": {
                            "X": 300.0,
                            "Y": 385.0
                        },
                        "Size": {
                            "Height": 220.0,
                            "Width": 65.0
                        }
                    }
                }
            }
        ]
    },
    "TemplatePath": "templates/template_2.json"
}"
 ```




 Response

```html 
* Response will contain storage path and url to resultant template file
{
    "url": "https://api.groupdocs.cloud/v1.0/parser/storage/file/templates/template_2.json",
    "templatePath": "templates/template_2.json"

 ```















```html 

* First get JSON Web Token
* Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&#x26;client_id#xxxx&#x26;client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
* cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/parser/template" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>" \
-d "{
    "Template": {
        "Fields": [
            {
                "FieldName": "Address",
                "FieldPosition": {
                    "FieldPositionType": "Fixed",
                    "Rectangle": {
                        "Position": {
                            "X": 13.0,
                            "Y": 35.0
                        },
                        "Size": {
                            "Height": 10.0,
                            "Width": 100.0
                        }
                    },
                    "MatchCase": false,
                    "IsLeftLinked": false,
                    "IsRightLinked": false,
                    "IsTopLinked": false,
                    "IsBottomLinked": false,
                    "AutoScale": false
                }
            },
            {
                "FieldName": "Company",
                "FieldPosition": {
                    "FieldPositionType": "Linked",
                    "MatchCase": false,
                    "LinkedFieldName": "Address",
                    "IsLeftLinked": false,
                    "IsRightLinked": false,
                    "IsTopLinked": false,
                    "IsBottomLinked": true,
                    "SearchArea": {
                        "Height": 15.0,
                        "Width": 100.0
                    },
                    "AutoScale": true
                }
            }
        ],
        "Tables": [
            {
                "TableName": "Totals",
                "DetectorParameters": {
                    "Rectangle": {
                        "Position": {
                            "X": 300.0,
                            "Y": 385.0
                        },
                        "Size": {
                            "Height": 220.0,
                            "Width": 65.0
                        }
                    }
                }
            }
        ]
    },
    "TemplatePath": "templates/template_2.json"
}"

 ```






 Response

```html 
* Response will contain storage path and url to resultant template file
{
    "url": "https://api.groupdocs.cloud/v1.0/parser/storage/file/templates/template_2.json",
    "templatePath": "templates/template_2.json"

 ```



  



# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "parser/getting-started/available-sdks.md" >}})) article to learn how to add an SDK to your project.
|---|---|---|---

## Create or Update Template Examples ##



 C#




{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Create_Update_Template.cs >}}





 Java




{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Create_Update_Template.java >}}






