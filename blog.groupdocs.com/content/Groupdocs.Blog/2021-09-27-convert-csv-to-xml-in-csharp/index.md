---
title: 'Convert CSV to XML in C#'
date: Mon, 27 Sep 2021 12:59:00 +0000
draft: false
url: /2021/09/27/convert-csv-to-xml-in-csharp/
author: 'Shoaib Khan'
summary: 'CSV and XML are among the most popular file formats used by developers. These formats are normally used to store and exchange data within and between applications. It is often required to convert one format into another before storing or transmitting the information. In this article, you will find **how to programmatically convert the CSV (comma-separated values) file into XML format using C#**.

The article will cover the following topics:

*   .NET API - CSV to XML Conversion
*   How to Convert CSV to XML in C#'
tags: ['Convert CSV to XML', 'Convert CSV to XML in CSharp', 'CSV to XML', 'CSV to XML in CSharp', ]
categories: ['GroupDocs.Conversion Product Family']
---

CSV and XML are among the most popular file formats used by developers. These formats are normally used to store and exchange data within and between applications. It is often required to convert one format into another before storing or transmitting the information. In this article, you will find **how to programmatically convert the CSV (comma-separated values) file into XML format using C#**.



{{< figure align=center src="images/convert-csv-to-xml-using-csharp.jpg" alt="Convert CSV to XML using CSharp">}}


The article covers the following topics:

*   [.NET API - CSV to XML Conversion](#csv-to-xml-dotnet-api)
*   [How to Convert CSV to XML in C#](#csv-to-xml)

## .NET API for CSV to XML Conversion {#csv-to-xml-dotnet-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) provides APIs that allow the CSV and XML files conversions. In this article, we will use the .NET API of GroupDocs.Conversion for converting the CSV format data into XML format using C#. Additionally, the API supports many other file formats for conversion like word-processing documents, spreadsheets, presentations, eBooks, images, etc.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/conversion) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert CSV to XML in C# {#csv-to-xml}

The CSV files can be viewed and visually edited using editors like MS Excel. The image shows the CSV data that I have used for the conversion. There are many CSV to XML converters available online, however, the code mentioned in this section can empower your .NET applications with this simple conversion.



{{< figure align=center src="images/csv-sample-file-opened-in-excel.jpg" alt="CSV Sample file opened in Excel">}}


The following steps guide you to convert the provided data of CSV format into XML format.

*   Load the CSV file using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Set the conversion format as XML using the [DataConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/dataconvertoptions).
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to get the XML format data from the loaded CSV file.

The following source code converts the CSV file to XML format using C#.

{{< gist GroupDocsGists 240c47d8a3ab8debabd13be9a83eac3a "ConvertCsvToXML.cs" >}}

The output of the above code is as follows. I am sharing the part of the XML file for you to get an idea of the XML output.

```
<DocumentElement>
  <Sheet1>
    <Employee>David</Employee>
    <Quarter>1</Quarter>
    <Product>Maxilaku</Product>
    <Continent>Asia</Continent>
    <Country>China</Country>
    <Sale>2000</Sale>
  </Sheet1>
  <Sheet1>
    <Employee>David</Employee>
    ...
  </Sheet1>
  <Sheet1>
    ...
  </Sheet1>
</DocumentElement>
```

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To sum up, we discussed the conversion of CSV data into XML format within the .NET applications using C#. To build your own conversion app, you may learn more about the Conversion Automation .NET API using the [documentation](https://docs.groupdocs.com/conversion/net/). The best is to experience the examples available on [GitHub](https://github.com/groupdocs-conversion). Contact us for any query via the [forum](https://forum.groupdocs.com/).

## See Also

*   [JSON to XML Conversion in C#](https://blog.groupdocs.com/2021/09/11/convert-json-to-xml-in-csharp/)
*   [Convert JSON to CSV and CSV to JSON using C#](https://blog.groupdocs.com/2021/06/18/convert-json-and-csv-in-csharp/)
*   [Convert Excel to CSV and CSV to Excel Formats in C#](https://blog.groupdocs.com/2021/08/18/convert-excel-xls-xlsx-and-csv-in-csharp/)




