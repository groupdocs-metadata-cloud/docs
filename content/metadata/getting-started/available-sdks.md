---
id: "available-sdks"
url: "metadata/available-sdks"
title: "Available SDKs"
productName: "GroupDocs.Metadata Cloud"
weight: 4
description: ""
keywords: ""
---


## GroupDocs.Metadata Cloud SDKs

GroupDocs.Metadata Cloud is a modern REST-oriented API, that allows easy integration into existing systems.

## Why use an SDK?

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project.

## SDK benefits

Our supported SDKs are 100% tested and out of the box running. These SDKs are open source and have the MIT license. You can use them and even customize them for absolutely free of charge.

## Supported SDKs

 .NET
**GroupDocs.Metadata Cloud SDK for .NET** allows you to incorporate GroupDocs.Metadata Cloud services in your .NET applications quickly and easily.

Install **[GroupDocs.Metadata-Cloud](https://www.nuget.org/packages/GroupDocs.Metadata-Cloud/)** via NuGet from Package Manager:

```html
PM> Install-Package GroupDocs.Metadata-Cloud
```

{{< alert style="info" >}}
Complete source code of GroupDocs.Metadata Cloud SDK for .Net is freely available on the [GitHub](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-dotnet).
{{< /alert >}}

{{< alert style="info" >}}Please see the GroupDocs.Metadata Cloud SDK for .NET [Examples here](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-dotnet-samples/tree/master/Examples).{{< /alert >}}

Java **GroupDocs.Metadata Cloud SDK for Java** allows you to incorporate GroupDocs.Metadata Cloud services in your Java applications quickly and easily.

You can directly include the source code of GroupDocs.Metadata Cloud SDK for Java in your own project, the source code is available from [here](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-java).

Alternatively, you can use **[Maven](https://releases.groupdocs.cloud/java/repo/com/groupdocs/groupdocs-metadata-cloud/)** to include in your Java project. Below are the steps for Maven.

**GroupDocs Maven Repository**

```xml
<repository>
    <id>groupdocs-artifact-repository</id>
    <name>GroupDocs Artifact Repository</name>
    <url>https://releases.groupdocs.cloud/java/repo/</url>
</repository>
```

**Maven Dependency**

```xml
<dependency>
    <groupId>com.groupdocs</groupId>
    <artifactId>groupdocs-metadata-cloud</artifactId>    
    <version>19.10</version>
    <scope>compile</scope>
</dependency>
```

**Get Sources and Javadocs**

**Maven**

```bash
mvn dependency:sources
mvn dependency:resolve -Dclassifier#javadoc
```

**Eclipse IDE**

```bash
mvn eclipse:eclipse -DdownloadSources#true
mvn eclipse:eclipse -DdownloadSources#true -DdownloadJavadocs#false
```

**pom.xml**

```xml
<build>
    <plugins>
        <plugin>      
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-eclipse-plugin</artifactId>
            <configuration>          
                <downloadSources>true</downloadSources>        
                <downloadJavadocs>false</downloadJavadocs>
            </configuration>
        </plugin>
    </plugins>
</build>
```

**Direct Download**

{{< alert style="info" >}}
Complete source code of GroupDocs.Metadata Cloud SDK for Java is freely available on the [GitHub](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-java).
{{< /alert >}}

{{< alert style="info" >}}Please see the GroupDocs.Metadata Cloud SDK for Java [Examples here](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-java/tree/master/src/test/java/com/groupdocs/cloud/metadata/api).{{< /alert >}}
