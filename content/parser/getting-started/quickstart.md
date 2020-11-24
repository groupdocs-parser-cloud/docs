---
id: "quickstart"
url: "parser/quickstart"
title: "Quickstart"
productName: "GroupDocs.Parser Cloud"
weight: 2
description: ""
keywords: ""
---

# Create an account #

Creating an account is very simple. Go to [Dashboard](https://dashboard.groupdocs.cloud) to create a free account.\
We're using Single Sign On across our websites, therefore, if you already have an account with our services, you can use it to also acccess the [Dashboard](https://dashboard.groupdocs.cloud).

# Create an API client app #

Before you can make any requests to GroupDocs Cloud API you need to get a **Client Id** and a **Client Secret**. This will will be used to invoke GroupDocs Cloud API.

You can get it by creating a new [Application](https://dashboard.groupdocs.cloud/applications).

# Install the SDK of your choice #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project.

Please check [Available SDKs]({{< ref "parser/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

# Make an API request from the SDK of your choice #

UUse the **Client Id** and the **Client Secret** from the API app client you created in step one and replace it in the corresponding code. Below is an example demonstrating how to get a list of all supported file formats in GroupDocs.Parser Cloud.

{{< alert style="info" >}}The GitHub repository for [GroupDocs.Parser Cloud](https://github.com/groupdocs-parser-cloud) has a complete set of examples, demonstrating our API capabilities.{{< /alert >}}


{{< tabs tabTotal="1" tabID="10" tabName1="C#" >}} {{< tab tabNum="1" >}}

```csharp

// For complete examples and data files, please go to https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-dotnet-samples
string ClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
string ClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud

var configuration = new Configuration(ClientId, ClientSecret);

var apiInstance = new InfoApi(configuration);
var response = apiInstance.GetSupportedFileFormats();

```

{{< /tab >}}

{{< /tabs >}}