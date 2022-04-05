---
title: 'Convert Excel to CSV and CSV to Excel Formats in C#'
date: Wed, 18 Aug 2021 03:39:00 +0000
draft: false
url: /2021/08/18/convert-excel-xls-xlsx-and-csv-in-csharp/
author: 'Shoaib Khan'
summary: 'XLS and XLSX are the most used and well-known formats of MS Excel spreadsheets. You must be well aware of the enhanced capabilities and countless formatting options of Microsoft Office for these formats during this century. On the other hand, **CSV** files are the comma-separated-values, normally used to store tabular data without formatting. These files can be viewed in any text editor and also in MS Excel for tabular format. This article discusses the conversion of the Excel spreadsheets of **XLS/XLSX format into CSV** format and **CSV to XLS/XLSX **format programmatically **using C#**.

The following topics are covered in this article:

*   .NET API for XLS/XLSX and CSV Conversion
*   Excel to CSV Conversion
*   CSV to Excel Conversion'
tags: ['Convert XLS and CSV in C#', 'CSV to Excel', 'CSV to Excel in C#', 'CSV to XLSX in C#', 'Excel to CSV', 'Excel to CSV in C#', 'XLSX to CSV in C#']
categories: ['GroupDocs.Conversion Product Family']
---



{{< figure align=center src="images/convert-xlsx-to-csv-and-csv-to-excel-in-csharp.jpg" alt="Convert XLS XLSX to CSV in C#">}}


XLS and XLSX are the most used and well-known formats of MS Excel spreadsheets. You must be well aware of the enhanced capabilities and countless formatting options of Microsoft Office for these formats during this century. On the other hand, **CSV** files are the comma-separated values, normally used to store tabular data without formatting. These files can be viewed in any text editor and also in MS Excel for tabular format. This article guides to convert Excel spreadsheets of **XLS/XLSX format into CSV** format and **CSV to XLS/XLSX **format programmatically **using C#**.

The following topics are covered below:

*   [.NET API for XLS/XLSX and CSV Conversion](#excel-csv-dotnet-api)
*   [Excel to CSV Conversion](#excel-to-csv)
*   [CSV to Excel Conversion](#csv-to-excel)

## .NET API for Excel Files and CSV Conversion {#excel-csv-dotnet-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) provides a .NET API that allows automating the conversion of various documents and image file formats into one another. I will be using this API to convert XLSX into CSV and then CSV into XLS or XLSX using C#. Along with the spreadsheet formats, the API supports [back and forth conversion of many other document and image formats](https://docs.groupdocs.com/conversion/net/supported-document-formats/) like word-processing documents, presentations, eBooks, JPG, PNG, WebP, and many more.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/conversion) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert Excel (XLS/XLSX) to CSV in C# {#excel-to-csv}

Let's start with the tabular and well-formatted data in XLS or XLSX format, and convert it into unformatted comma-separated CSV format. The following steps allow converting the XLS or XLSX format to CSV within the .NET applications.

*   Load the Excel file (XLS or XLSX) using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Set the starting worksheet number and sheet count. (Optional)
*   Set the conversion format of the output file as CSV using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/spreadsheetconvertoptions).
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to transform the spreadsheet data or and specific pages into CSV format.

The following code shows how to convert XLS or XLSX into CSV format in C#.

{{< gist GroupDocsGists 53e4d00e8195ad3eb4ba03fffc4e9315 "ConvertExcelToCSV.cs" >}}

## Convert CSV to Excel (XLS/XLSX) in C# {#csv-to-excel}

On the contrary, if you have the comma-separated data and you want to convert it into a well-formatted tabular format, you need to convert that CSV data into XLS or XLSX format. The following steps show how to convert the CSV file into MS Excel XLSX format using C#.

*   Prepare the loading options for CSV file and define separator.
*   Load the CSV using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Set the conversion format to XLSX using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/spreadsheetconvertoptions).
*   Use the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to get the CSV data transformed into XLSX format.

The following code shows how to convert your CSV file into XLSX format in C#.

{{< gist GroupDocsGists 53e4d00e8195ad3eb4ba03fffc4e9315 "ConvertCsvToExcel.cs" >}}

Just set the conversion format accordingly and provide the appropriate file name with the extension for the XLS or any other file format.

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up the article, you learned back and forth conversion of MS Excel spreadsheets XLS/XLSX and CSV files using C#. You can learn more about the .NET Conversion Automation API using the documentation, or by experiencing the examples available on GitHub. Reach us for any query via the [forum](https://forum.groupdocs.com/).

## Related Article

*   [Convert CSV to Excel, and (XLS or XLSX) to CSV in Java](https://blog.groupdocs.com/2021/07/31/convert-csv-and-excel-xls-xlsx-in-java/)

## See Also

*   [Generate Reports from CSV Data using C#](https://blog.groupdocs.com/2021/08/15/generate-reports-from-csv-data-in-csharp/)
*   [Convert Excel Spreadsheets to PDF using C#](https://blog.groupdocs.com/2021/11/14/convert-excel-spreadsheets-to-pdf-using-csharp/)
*   [Convert JSON to CSV and CSV to JSON using C#](https://blog.groupdocs.com/2021/06/18/convert-json-and-csv-in-csharp/)
*   [Insert OLE Objects in Word, Excel, PowerPoint with C#](https://blog.groupdocs.com/2020/05/16/insert-ole-objects-in-word-excel-powerpoint-with-csharp/)




