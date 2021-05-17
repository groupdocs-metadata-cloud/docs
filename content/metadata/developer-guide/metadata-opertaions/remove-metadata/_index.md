---
id: "remove-metadata"
url: "metadata/remove-metadata"
title: "Remove Metadata"
productName: "GroupDocs.Metadata Cloud"
weight: 4
description: ""
keywords: ""
---





## Introduction ##

This REST API allows to remove metadata from the documents.

With this API you can search metadata to remove with following features:

* There are many ways to specify what property should be removed. You could search for properties to add by:
  * name (a part of name, exact phrase, regex match. All names matching is ignorecase);
  * tag (exact tag, possible tag name).
  * values of different types:
    * string;
    * datetime;
    * integer;
    * double;
    * boolean;

The table below contains the full list of properties that can be specified when removing metadata to the document.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage. |Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.
|OutputFolder|The folder for the resultant file.|Default value is "/remove_metadata"
|SearchCriteria|Options to remove properties.|Required
|SearchCriteria.TagOptions|Options to find property by tag.|Required if searching by tag
|TagOptions.PossibleName|A part or a possible tag name.|If a part of tag name is known
|ExactTag|Options to specify exact tag.|If tag and category name is known. More accurate
|ExactTag.Name|Name of the tag.|Required
|ExactTag.Category|Category of the tag.|Required
|SearchCriteria.NameOptions|Options to find property by name.|Required if searching by name
|NameOptions.Value|The value for name matching.|Required
|NameOptions.MatchOptions|Specifies how to find property name.|
|MatchOptions.ExactPhrase|Value indicating whether to match exact string phrase.|
|MatchOptions.IsRegex|Value indicating whether to match by regular expression.|
|SearchCriteria.ValueOptions|Options to find property by value.|Required if searching by value
|ValueOptions.Value|Specifies value of property to find.|Required
|ValueOptions.Type|Type of property value.|String is default. Possible types: string;datetime;integer;double;boolean.

### Resource URI ###

```html
HTTP POST ~/metadata/remove
```

[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Metadata/Remove) lets you call this REST API directly from the browser.  

### Use Cases ###
