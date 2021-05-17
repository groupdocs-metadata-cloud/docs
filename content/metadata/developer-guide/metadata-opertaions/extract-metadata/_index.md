---
id: "extract-metadata"
url: "metadata/extract-metadata"
title: "Extract Metadata"
productName: "GroupDocs.Metadata Cloud"
weight: 1
description: ""
keywords: ""
---





## Introduction ##

This REST API allows to extract metadata from the documents.

With this API you can extract metadata with following features:

* Extract whole metadata properties tree;
* Extract properties with specified tag;
* Extract properties with specified name;
* Extract properties with specified value;

The table below contains the full list of properties that can be specified when extracting metadata from the document.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage. |Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.
|SearchCriteria|Options to find properties.|Required
|SearchCriteria.TagOptions|Options to find property by tag.|Required if searching by tag
|TagOptions.PossibleName|A part or a possible tag name.|If a part of tag name is known
|TagOptions.ExactTag|Options to specify exact tag.|If tag and category name is known. More accurate
|ExactTag.Name|Name of the tag.|Required
|ExactTag.Category|Category of the tag.|Required
|SearchCriteria.NameOptions|Options to find property by name.|Required if searching by name
|NameOptions.Value|The value for name matching.|Required
|NameOptions.MatchOptions|Specifies how to find property name.|
|MatchOptions.ExactPhrase|Value indicating whether to match exact string phrase.|
|MatchOptions.IsRegex|Value indicating whether to match by regular expression.|
|SearchCriteria.ValueOptions|Options to find property by value.|Required if searching by value
|ValueOptions.Value|Specifies value of property to find.|Required
|ValueOptions.Type|Type of property value.|

### Resource URI ###

```html
HTTP POST ~/metadata
```

[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Metadata/Extract) lets you call this REST API directly from the browser.  

### Use Cases ###
