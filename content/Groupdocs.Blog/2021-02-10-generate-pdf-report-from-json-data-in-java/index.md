---
title: 'Generate Reports from JSON Data in Java'
date: Wed, 10 Feb 2021 18:40:00 +0000
draft: false
url: /2021/02/10/generate-pdf-report-from-json-data-in-java/
author: 'Shoaib Khan'
summary: 'JSON is a formatted and readable data interchange format to transmit data with attributes. However, the large data in JSON format is not very presentable and easily understandable. We mostly need to convert the large JSON data into a presentable format. This article will guide you to **convert JSON data into PDF report in Java** using a simple template.

[Continue Reading ...](https://blog.groupdocs.com/2021/02/10/generate-pdf-report-from-json-data-in-java)'
tags: ['Convert JSON to PDF in Java', 'Generate PDF report from JSON', 'Generate PDF Report in Java', 'JSON to PDF using Template in Java']
categories: ['GroupDocs.Assembly Product Family']
---

JSON is a formatted and readable data interchange format to transmit data with attributes. However, the large data in JSON format is not very presentable and easily understandable. We mostly need to convert the large JSON data into a presentable format. This article will guide you to **convert JSON data into PDF and MS Word reports in Java** using a simple template.

## Report Generation Java API

I will be using [GroupDocs.Assembly for Java](https://products.groupdocs.com/assembly/java) API to generate reports from the provided **JSON** data and template in **DOCX** and **TXT** format. It also supports automatic report generation in multiple formats from **CSV, XML** data sources.

### Download or Configure

You may download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/assembly/java), or just get the repository and dependency configurations for the pox.xml of your **maven-based** Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-assembly</artifactId>
        <version>21.1</version> 
</dependency>
```

## Generate PDF Report from JSON Data in Java

Let's quickly jumps to the steps that will lead you to convert JSON data into the formatted PDF report.

*   Get JSON data source
*   Define template according to JSON data
*   Provide JSON data source and template to simple java code for report generation.



{{< figure align=center src="images/json-to-pdf-report-in-java.jpg" alt="JSON to PDF Report in Java">}}


### JSON Data

For the PDF report generation, I will be using the following sample JSON data of managers and their respective clients and details.

```
\[
	{
		"Name":"John Smith","Contract":\[
		{"Client":{"Name":"A Company"},"Price":1200000},
		{"Client":{"Name":"B Ltd."},"Price":750000},
		{"Client":{"Name":"C & D"},"Price":350000}\]
	},
	{
		"Name":"Tony Anderson","Contract":\[
		{"Client":{"Name":"E Corp."},"Price":650000},
		{"Client":{"Name":"F & Partners"},"Price":550000}\]
	},
	{
		"Name":"July James","Contract":\[
		{"Client":{"Name":"G & Co."},"Price":350000},
		{"Client":{"Name":"H Group"},"Price":250000},
		{"Client":{"Name":"I & Sons"},"Price":100000},
		{"Client":{"Name":"J Ent."},"Price":100000}\]
	}
\]
```

### Template

Define the following template in TXT or DOCX format. This will allow to iterate over Managers and their respective Clients and their details. After that, you can jump to code for report generation.

```
<<foreach [in managers]>>Manager: <<[Name]>>
Contracts:
<<foreach [in Contract]>>- <<[Client.Name]>> ($<<[Price]>>)
<</foreach>>
<</foreach>>
```

### Java Steps to Generate PDF Report from JSON

Following steps and Java code allows automatic conversion of JSON data into PDF report as per defined template.

*   Define JSON data file, .txt template file, and PDF output report file paths.
*   Instantiate [JsonDataSoure](https://apireference.groupdocs.com/assembly/java/com.groupdocs.assembly/JsonDataSource) with JSON data file.
*   Create [DataSourceInfo](https://apireference.groupdocs.com/assembly/java/com.groupdocs.assembly/DataSourceInfo) with defined JsonDataSource.
*   Call the _**assembleDocument**_ method of the [DocumentAssembler](https://apireference.groupdocs.com/assembly/java/com.groupdocs.assembly/DocumentAssembler) class to generate the PDF report from the provided JSON data and defined template.

{{< gist GroupDocsGists 7aa7fe4f1a969e13339ace6ba8c51906 "GeneratePdfReportFromJSON.java" >}}

## Generate MS Word Report from JSON data in Java

Similarly, like the above PDF report generation, you can easily create the DOCX report by:

*   Defining the same template in DOCX format.
*   Set the output report document format as DOCX.
*   The rest of the code will remain the same to generate MS Word DOCX report from the JSON data.

{{< gist GroupDocsGists 7aa7fe4f1a969e13339ace6ba8c51906 "GenerateWordReportFromJsonWIthTemplate.java" >}}

For more details, options, and examples, you can go through the [documentation](https://docs.groupdocs.com/assembly/java/) and [GitHub](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-Java) repository. In case of further queries and ambiguities, contact the free support on the [forum](https://forum.groupdocs.com/c/assembly).

## Conclusion

I hope you will feel comfortable building your own Java-based application to generate reports by converting JSON data to PDF format. Similarly, you can generate reports in other formats like DOCX using other data sources like CSV and XML.

## See Also

*   [Generate Reports from JSON Data in C#](https://blog.groupdocs.com/2021/03/20/generate-reports-from-json-data-in-csharp/)




