---
title: 'Convert JSON to CSV and CSV to JSON using C#'
date: Fri, 18 Jun 2021 12:25:49 +0000
draft: false
url: /2021/06/18/convert-json-and-csv-in-csharp/
author: 'Shoaib Khan'
summary: '**JSON** (JavaScript Object Notation) is a human-readable structured data format. It is widely used in APIs, applications, and configurations for storing and passing the data. **CSV** contains the comma-separated values, normally used to store tabular data that can be perfectly displayed using spreadsheet applications like MS Excel. To transfer the tabular data or store the received structured data into tabular form, requires converting formats into one another. This article discusses the conversion of **JSON to CSV** format and **CSV to JSON** format programmatically **using C#** for your .NET applications.'
tags: ['Convert CSV in CSharp', 'Convert JSON in CSharp', 'CSV to JSON in CSharp', 'JSON to CSV in CSharp']
categories: ['GroupDocs.Conversion Product Family']
---



{{< figure align=center src="images/convert-csv-and-json-in-csharp.jpg" alt="Convert to CSV and JSON in CSharp .NET">}}


**JSON** (JavaScript Object Notation) is a human-readable structured data format. It is widely used in APIs, applications, and configurations for storing and passing the data. **CSV** contains the comma-separated values, normally used to store tabular data that can be perfectly displayed using spreadsheet applications like MS Excel. To transfer the tabular data or store the received structured data into tabular form, requires converting formats into one another. This article discusses the conversion of **JSON to CSV** format and **CSV to JSON** format programmatically **using C#** for your .NET applications.

The following topics are covered below:

*   [.NET API for JSON and CSV Conversion](#json-csv-dotnet-api)
*   [JSON to CSV Conversion](#json-to-csv)
*   [CSV to JSON Conversion](#csv-to-json)

## .NET API for JSON and CSV Conversion {#json-csv-dotnet-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) has APIs that allow the conversion of JSON and CSV files into each other. In this article, we will use the .NET API of GroupDocs.Conversion for converting JSON into CSV and then CSV into JSON using C#. Additionally, the API allows the [back and forth conversion of various other document formats](https://docs.groupdocs.com/conversion/net/supported-document-formats/) like word-processing documents, spreadsheets, presentations, eBooks, images, and many more.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/conversion) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert JSON to CSV in C# {#json-to-csv}

The following steps allow converting the JSON files to CSV format within the .NET applications.

*   Load the JSON using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Set the conversion format to CSV using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/spreadsheetconvertoptions).
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to transform the JSON data to CSV format.

The following code shows how to convert JSON to CSV format using C#.

{{< gist GroupDocsGists 499489bd99efab8b475e447083d377a6 "ConvertJsonToCSV.cs" >}}

## Convert CSV to JSON in C# {#csv-to-json}

The following steps allow converting the CSV files to JSON format within the .NET application.

*   Prepare the load options for loading the CSV file.
*   Load the CSV using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Set the conversion format to JSON using [DataConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/dataconvertoptions).
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to get the CSV data transformed into JSON format.

The following code shows how to convert your CSV file into JSON format using C#.

{{< gist GroupDocsGists 499489bd99efab8b475e447083d377a6 "ConvertCsvToJSON.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you learned how to convert the JSON files to CSV format and also the conversion of CSV files to JSON format programmatically using C#. You can learn more about the .NET Conversion API using the [documentation](https://docs.groupdocs.com/conversion/net/), or by examples available on [GitHub](https://github.com/groupdocs-conversion). Get in touch with us at the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert Excel to CSV and CSV to Excel Formats in C#](https://blog.groupdocs.com/2021/08/18/convert-excel-xls-xlsx-and-csv-in-csharp/)
*   [Generate Reports from JSON Data in C#](https://blog.groupdocs.com/2021/03/20/generate-reports-from-json-data-in-csharp/)
*   [Generate Reports from CSV and XML Data in C#](https://blog.groupdocs.com/2019/10/21/generate-reports-from-csv-xml-in-csharp/)




