---
id: "add-metadata"
url: "metadata/add-metadata"
title: "Add Metadata"
productName: "GroupDocs.Metadata Cloud"
weight: 2
description: ""
keywords: ""
---





# Introduction #

This REST API allows to add metadata to the documents.

With this API you can add metadata with following features:

* Metadata properties could contain different types of values:
** string;
** datetime;
** integer;
** double;
** boolean;
* There are many ways to specify what property should be added. You could search for properties to add by:
** name (a part of name, exact phrase, regex match. All names matching is ignorecase);
** tag (exact tag, possible tag name).

The table below contains the full list of properties that can be specified when adding metadata to the document.


|Name|Description|Comment
|FileInfo.FilePath|The path of the document, located in the storage. |Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.
|OutputFolder|The folder for the resultant file.|Default value is "/add_metadata"
|Properties|Collection of properties to add.|Required
|Properties.Value|The value of the added property.|Required
|Properties.Type|Type of the added value.|String is default. Possible type values: string, datetime, integer, double, boolean
|SearchCriteria|Options to define metadata property tag or name.|Required
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

## Resource URI ##


```html 

HTTP POST ~/metadata/add

 ```


[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Metadata/Add) lets you call this REST API directly from the browser.  

## Use Cases ##

