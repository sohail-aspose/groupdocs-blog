---
title: 'Generate Reports from XML Data in Java'
date: Sat, 10 Jul 2021 10:01:00 +0000
draft: false
url: /2021/07/10/generate-reports-from-xml-data-in-java/
author: 'Shoaib Khan'
summary: '**XML** is an e**X**tensive **M**arkup **L**anguage that is self-descriptive, W3C Recommended, and designed to store and transport data. After receiving the data in XML format, as a developer, you can convert it into any other better human-readable format like PDF or MS Word document. This article will guide you to convert XML data into PDF and MS Word reports in Java using simple templates.

The following topics are discussed in this article:

*   Java API for Generating Reports
*   PDF Report from XML Data using Java
*   MS Word DOC/DOCX Report from XML Data using Java'
tags: ['Convert XML to DOCX in Java', 'Convert XML to PDF in Java', 'Generate PDF Report from XML', 'Generate Reports in Java', 'XML to DOCX in Java', 'XML to PDF in Java']
categories: ['GroupDocs.Assembly Product Family']
---

**XML** is an e**X**tensive **M**arkup **L**anguage that is self-descriptive, W3C Recommended, and designed to store and transport data. After receiving the data in XML format, as a developer, you can convert it into any other better human-readable format like PDF or MS Word document. This article will guide you to convert XML data into PDF and MS Word reports in Java using simple templates.

The following topics are discussed below:

*   [Java API for Generating Reports](#generate-report-java-api)
*   [PDF Report from XML Data using Java](#xml-to-pdf-report-in-java)
*   [MS Word DOC/DOCX Report from XML Data using Java](#xml-to-word-report-in-java)

## Report Generation Java API - XML to PDF and WORD {#generate-report-java-api}

[GroupDocs.Assembly](https://products.groupdocs.com/assembly) provides Java API to automate the report generation from the **XML** data using **DOCX** or **TXT** template. It further supports the **JSON, CSV,** and other data sources to convert the data into presentable reports of different file formats.

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
        <version>21.4</version> 
</dependency>
```

## Generate PDF Report from XML Data in Java {#xml-to-pdf-report-in-java}

Let’s quickly jumps to the steps that will lead you to convert XML data into the formatted PDF report.

*   Load the XML data source
*   Define the template according to your XML data
*   Provide XML data source and template to a method for report generation.



{{< figure align=center src="images/xml-to-pdf-word-report-in-java.jpg" alt="XML to PDF Report in Java">}}


### XML Data

For the PDF report generation, the following XML sample data is used. It contains the data of managers and their respective clients with details.

```
<Managers>
	<Manager>
		<Name>John Smith</Name>
		<Contract>
			<Client>
				<Name>A Company</Name>
			</Client>
			<Price>1200000</Price>
		</Contract>
		<Contract>
		...
		</Contract>
		...
	</Manager>
	<Manager>
		<Name>Tony Anderson</Name>
		...
	</Manager>
	...
</Managers>
```

### Template

Define the following template in TXT or DOCX format. This allows iteration over Managers and their respective Clients. After that, use the code mentioned below for report generation.

```
<<foreach \[in managers\]>>Manager: <<\[Name\]>>
Contracts:
<<foreach \[in Contract\]>>- <<\[Client.Name\]>> ($<<\[Price\]>>)
<</foreach>>
<</foreach>>
```

### Java Steps to Generate PDF Report from XML

The following steps and the code allows automating the generation of PDF reports from the XML data as per the defined template.

*   Define XML data file, text template file, and PDF output report files.
*   Instantiate [XMLDataSoure](https://apireference.groupdocs.com/assembly/java/com.groupdocs.assembly/XmlDataSource) with XML data file.
*   Create [DataSourceInfo](https://apireference.groupdocs.com/assembly/java/com.groupdocs.assembly/DataSourceInfo) with defined XML data source.
*   Call the [assembleDocument](https://apireference.groupdocs.com/assembly/java/com.groupdocs.assembly/DocumentAssembler#assembleDocument-java.lang.String-java.lang.String-com.groupdocs.assembly.DataSourceInfo...-) method to generate the PDF report.

The following code implements the above steps and generates a PDF from the XML data source in Java.

{{< gist GroupDocsGists 836ca189a2cb4d2a7e5283c47a5a70ce "XmlToPdfReport.java" >}}

## Generate MS Word Report from XML data in Java {#xml-to-word-report-in-java}

Likewise, you can create the MS Word DOC/DOCX report from the same XML data in Java. There will be no difference, except to change the output file name.

*   Load the XML data file.
*   Defining the template in TXT or DOCX format.
*   Set the output report document format as DOCX.
*   Provide the XML data file, template, and output file path to DocumentAssembler to convert the XML to DOCX.

The following code converts the XML and generates the DOCX file using the defined template in Java.

{{< gist GroupDocsGists 836ca189a2cb4d2a7e5283c47a5a70ce "XmlToWordReport.java" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you have learned to convert your XML data into PDF format as a report in Java. Additionally, you have seen the report generation in DOC/DOCX format from the same XML using the template. After reading the series, Generate PDF and MS Word Reports from [**JSON**](https://blog.groupdocs.com/2021/02/10/generate-pdf-report-from-json-data-in-java/), [**CSV**](https://blog.groupdocs.com/2021/07/07/generate-reports-from-csv-data-in-java/), **XML**, you should be comfortable in building your own report builder Java application.

Similarly, you can convert many other data sources to report. For more details, options, and examples, you can visit [documentation](https://docs.groupdocs.com/assembly/java/) and the GitHub repository. In case of further queries, contact us via the [forum](https://forum.groupdocs.com/c/assembly).

## See Also

*   [Convert JSON Data to PDF or Word Report using Java](https://blog.groupdocs.com/2021/02/10/generate-pdf-report-from-json-data-in-java/)
*   [Transform CSV Data into PDF or Word Report using Java](https://blog.groupdocs.com/2021/07/07/generate-reports-from-csv-data-in-java/)




