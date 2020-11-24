---
id: "features-overview"
url: "metadata/features-overview"
title: "Features Overview"
productName: "GroupDocs.Metadata Cloud"
weight: 1
description: ""
keywords: ""
---

# Overview #

GroupDocs.Metadata Cloud is a powerful and easy to use metadata management REST API which allows users to read and edit metadata associated with various document, image, audio, video and many other formats.

The API also provides operations to extract metadata, add, search, modify and remove metadata in supported file formats. 

Below you may find an overview for the most valuable features.

## Extracting Metadata ##

Using the GroupDocs.Metadata Cloud you can extract desired metadata properties from files of different types. You don't need to worry about the exact file format and metadata standards it can deal with. The same API works for all supported formats in the same way.

Most commonly used metadata properties are marked with tags that allow searching them across all supported files in various metadata packages. To obtain all possible metadata tags, please use tags endpoint (read more at [Get metadata tags information]({{< ref "metadata/developer-guide/info-operations/get-metadata-tags-information.md" >}}) article).

## Adding Metadata ##

GroupDocs.Metadata Cloud allows to add metadata to supported document formats.

Please specify search criteria and the add method will examine all available metadata packages and try to pick up a known metadata property that would satisfy the specified search criteria and add the specified value.

## Modifying Metadata ##

GroupDocs.Metadata Cloud allows to modify metadata in supported document formats.

The modify method accepts the same search criteria object as other methods. It is handy to retrieve metadata with a search criteria and use the same criteria for mofifying them.

## Removing Metadata ##

GroupDocs.Metadata Cloud allows to remove metadata from supported document formats.

Please specify search criteria and metadata will be removed. Please note that not all metadata properties in a file are marked with tags. Some file formats and metadata standards allow adding fully custom properties that can't be properly tagged. In such cases it is convenient to use the name of the property to locate and remove it.

# API Endpoint Groups Overview #


|Endpoint Group|Description
|Metadata|Contains endpoints for add, remove, set and extract metadata.
|Info|Contains endpoints for obtaining list of formats supported by GroupDocs.Metadata Cloud, getting basic information about document and its pages, retrieve metadata tags information.
|File|Contains endpoints for upload, download, copy, move, delete files in the storage
|Folder|Contains endpoints for create, copy, move, delete folders in the storage
|Storage|Contains endpoints for obtaining storage information and file information

# Security and Authentication #

The GroupDocs.Metadata Cloud API is secured and requires authentication. Two keys Client Id and Client Secret are required for Authentication which can be created at the [Dashboard](http://dashboard.groupdocs.cloud).
Check [Authenticating API Requests]({{< ref "total/getting-started/overview-rest-api/authenticating-api-requests.md" >}}) article for complete example.

# SDKs #

Checkout our GitHub [repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata SDKs along with working examples, to get you started in no time. 

At the moment following SDKs are provided: 

* .NET 2.0 ([Sources](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-dotnet), [NuGet Package](https://www.nuget.org/packages/GroupDocs.Metadata-Cloud))
* Java ([Sources](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-java), Jar)

# API Explorer #

The easiest way to try out our API right away in your browser! With the [GroupDocs Cloud API explorer](https://apireference.groupdocs.cloud/metadata/). This is a collection of Swagger documentation for the GroupDocs Cloud APIs. You can get information about all the resources in the API. It also provides testing and interactivity to our API endpoint documentation.