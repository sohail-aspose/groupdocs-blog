---
title: 'Generate Reports from CSV Data using C#'
date: Sun, 15 Aug 2021 10:50:32 +0000
draft: false
url: /2021/08/15/generate-reports-from-csv-data-in-csharp/
author: 'Shoaib Khan'
summary: 'CSV ([Comma Separated Values](https://docs.fileformat.com/spreadsheet/csv/)) files are widely used for exchanging data among applications. When you want this data to be translated into presentable and meaningful information, you need to convert it into some other format. In one of our posts, we have seen [how to convert CSV data in Reports using Java](https://blog.groupdocs.com/2021/07/07/generate-reports-from-csv-data-in-java/). This article will guide you to **convert CSV data into PDF and MS Word DOC/DOCX reports using C#** using a simple template.'
tags: ['Convert CSV to PDF in CSharp', 'CSV to PDF using template', 'CSV to Word Report in CSharp', 'Generate PDF report from CSV', 'Generate Reports', 'generate reports in csharp', ]
categories: ['GroupDocs.Assembly Product Family']
---

CSV ([Comma Separated Values](https://docs.fileformat.com/spreadsheet/csv/)) files are widely used for exchanging data among applications. When you want this data to be translated into presentable and meaningful information, you need to convert it into some other format. In one of our posts, we have seen [how to convert CSV data in Reports using Java](https://blog.groupdocs.com/2021/07/07/generate-reports-from-csv-data-in-java/). This article will guide you to **convert CSV data into PDF and MS Word DOC/DOCX reports using C#** using a simple template.

The following topics are covered below:

*   [Report Generation .NET API](#report-generator-dotnet-api)
*   [Generate PDF Report from CSV Data](#csv-to-pdf-report-csharp)
*   [Generate MS Word Report from CSV data](#csv-to-docx-report-java)

## Report Generation .NET API {#report-generator-dotnet-api}

[GroupDocs.Assembly](https://products.groupdocs.com/assembly/java) provides the .NET reporting API to automate the report generation. In this article, I have used this [GroupDocs.Assembly for .NET](https://products.groupdocs.com/assembly/net/) for generating reports from the selected **CSV** data and a **TXT** format template. It also supports multiple data sources like **JSON, XML**, and also from **MS Word**, **Excel**, and **PowerPoint** files as data files.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/assembly/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.assembly).

```
PM> Install-Package GroupDocs.Assembly
```

## Generate PDF Report from CSV Data in C# {#csv-to-pdf-report-csharp}

Let's begin by transforming the comma-separated data into a presentable PDF. The following steps will guide you to convert the CSV data into a formatted PDF report.

*   Load CSV data source.
*   Define template according to the CSV data.
*   Provide CSV data source and template to simple method to generate PDF report.



{{< figure align=center src="images/csv-to-pdf-word-report-in-csharp.jpg" alt="CSV to PDF Report in C#">}}


### CSV Data

To get the PDF report, I will be using the following sample CSV data of different individuals along with their respective data of ages and date of birth.

```
Name,Age,Birth  
John Doe,32,4/1/1989 16:00  
Jane Doe,29,1/31/1992 7:00  
John Smith,53,3/8/1968 13:00
```

### Template

The next step would be to define the template in TXT or DOCX format. The following is the template that is used in this example and allows iterating the list of persons with their details.

```
<<foreach \[in persons\]>>Name: <<\[Name\]>>, Age: <<\[Age\]>>, Date of Birth: <<\[Birth\]:"dd.MM.yyyy">>
<</foreach>>
Average age: <<\[persons.Average(p => p.Age)\]>>
```

### Steps to Generate PDF Report from CSV in C#

The following steps guide about converting the CSV data into a PDF report according to the defined template using C# with the .NET Reporting API.

*   Define CSV data file, template file, and the PDF output file paths.
*   Instantiate [CsvDataSoure](https://apireference.groupdocs.com/net/assembly/groupdocs.assembly.data/csvdatasource) with CSV data file and loading options.
*   Create [DataSourceInfo](https://apireference.groupdocs.com/assembly/net/groupdocs.assembly/datasourceinfo) with the defined data source.
*   Using the [DocumentAssembler](https://apireference.groupdocs.com/assembly/net/groupdocs.assembly/documentassembler), call the [AssembleDocument](https://apireference.groupdocs.com/assembly/net/groupdocs.assembly/documentassembler/methods/assembledocument/index) method with defined template file, output file and DataSourceInfo to get the PDF report as output.

The following code shows how to convert CSV data to PDF report in C#.

{{< gist GroupDocsGists 39a6cdabd9133f9b8349b78e95b56a4b "GeneratePdfReportFromCSV.cs" >}}

## Generate MS Word Report from CSV data in C# {#csv-to-docx-report-java}

If you want any manual editing in the automated generated report, you can also get the output as an MS Word document. The process will be very similar to the above PDF report generation. The following steps will guide to generate the DOC/DOCX report from the CSV data:

*   Load the CSV data from file.
*   Defining the template in TXT or DOCX format.
*   Set the output report document format as DOC/DOCX.
*   Call the [AssembleDocument](https://apireference.groupdocs.com/assembly/net/groupdocs.assembly/documentassembler/methods/assembledocument/index) method to generate MS Word DOCX report from the CSV data.

The following code shows how to convert CSV data into a DOCX report using C#.

{{< gist GroupDocsGists 39a6cdabd9133f9b8349b78e95b56a4b "GenerateWordReportFromCSV.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you have learned to convert the CSV data into PDF and MS Word reports using C#. You must now be confident building your own .NET report generator application by converting CSV data into PDF format. Similarly, you can also generate reports using other data sources like JSON and XML.

For more about the API, you can visit [documentation](https://docs.groupdocs.com/assembly/net/) and the [GitHub](https://github.com/groupdocs-assembly) repository. In case of further queries and ambiguities, contact the free support on the [forum](https://forum.groupdocs.com/c/assembly).

## See Also

*   [Generate Reports from JSON Data using C#](https://blog.groupdocs.com/2021/03/20/generate-reports-from-json-data-in-csharp/)
*   [Generate Reports from CSV Data using Java](https://blog.groupdocs.com/2021/07/07/generate-reports-from-csv-data-in-java/)




