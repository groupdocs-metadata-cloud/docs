---
id: "set-metadata"
url: "metadata/set-metadata"
title: "Set Metadata"
productName: "GroupDocs.Metadata Cloud"
weight: 3
description: ""
keywords: ""
---





# Introduction #

This REST API allows to set metadata new values into existing properties of the documents.

With this API you can set metadata with following features:

* Metadata properties could contain different types of values:
** string;
** datetime;
** integer;
** double;
** boolean;
* There are many ways to specify what property should be edited. You could search for properties to set by:
** name (a part of name, exact phrase, regex match. All names matching is ignorecase);
** tag (exact tag, possible tag name);
** value.

The table below contains the full list of properties that can be specified when setting metadata to the document.


|Name|Description|Comment
|FileInfo.FilePath|The path of the document, located in the storage. |Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.
|OutputFolder|The folder for the resultant file.|Default value is "/add_metadata"
|Properties|Collection of properties to set.|Required
|Properties.NewValue|The value of the edited property.|Required
|Properties.Type|Type of the edited value.|String is default. Possible types: string;datetime;integer;double;boolean.
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
|SearchCriteria.ValueOptions|Options to find property by value.|Required if searching by value
|ValueOptions.Value|Specifies value of property to find.|Required
|ValueOptions.Type|Type of property value.|String is default. Possible types: string;datetime;integer;double;boolean.

## Resource URI ##


```html 

HTTP POST ~/metadata/set

 ```


[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Metadata/Set) lets you call this REST API directly from the browser.  

## Use Cases ##

