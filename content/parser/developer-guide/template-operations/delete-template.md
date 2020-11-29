---
id: "delete-template"
url: "parser/delete-template"
title: "Delete Template"
productName: "GroupDocs.Parser Cloud"
weight: 3
description: ""
keywords: ""
---






# Introduction #

This REST API provides the functionality to remove files which no more useful in Parse endpoint. You can use [storage methods]({{< ref "parser/developer-guide/storage-operations/_index.md" >}})) to remove template files as well.
|---|---

The table below contains the full list of properties.

 

|Name|Description|Comment
|---|---|---
|TemplatePath|The path of the template, located in the storage.|**Required.**
|FileInfo.StorageName|Storage name|It could be omitted for default storage.


## Resources ##

The following GroupDocs.Parser Cloud REST API resource has been used in the [Delete Template](https://apireference.groupdocs.cloud/parser/#/Template/DeleteTemplate) example.
|---|---

**Resource URI**

```html 

HTTP DELETE ~/template

 ```

## cURL Example ##

The following example demonstrates how to Delete a Template.





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
    "TemplatePath": "templates/template_1.json"
}"
 ```




 Response

```html 
* An empty response with '204 No Content' is returned to confirm deletion.
 ```






## SDKs ##

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "parser/getting-started/available-sdks.md" >}})) article to learn how to add an SDK to your project.
|---|---|---|---

### Delete Template Examples ###





 C#




{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Delete_Template.cs >}}







 Java




{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Delete_Template.java >}}







