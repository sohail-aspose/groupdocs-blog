---
title: 'Convert JSON to XML in C#'
date: Sat, 11 Sep 2021 09:17:00 +0000
draft: false
url: /2021/09/11/convert-json-to-xml-in-csharp/
author: 'Shoaib Khan'
summary: 'JSON and XML, both are the well known structured formats that are vastly used by developers to transmit data. There are many requirement where as a programmer, we need the conversion between JSON and XML data formats. In this article, you will learn how to convert JSON data into XML format using C#.

The following topics will be covered in this article:

*   .NET API for JSON and XML Conversion
*   Programmatically Convert JSON to XML'
tags: ['Convert JSON to XML', 'Convert JSON to XML in CSharp', 'JSON to XML', 'JSON to XML in CSharp']
categories: ['GroupDocs.Conversion Product Family']
---

JSON and XML, both are well-known structured formats that are vastly used by developers to transmit data. There are many requirements where, as a programmer, we need the conversion between JSON and XML data formats. In this article, you will learn **how to convert JSON data into XML format using C#**.



{{< figure align=center src="images/convert-json-to-xml-csharp.jpg" alt="Convert JSON to XML in CSharp">}}


The following topics are covered below:

*   [.NET API for JSON and XML Conversion](#json-xml-conversion-dotnet-api)
*   [Programmatically Convert JSON to XML](#json-to-xml)

## .NET API for JSON and XML Conversion {#json-xml-conversion-dotnet-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) provides a .NET API that allows automating the conversion of different documents, images, and other file formats into one another. I am using the same API here to convert JSON files into XML format using C#. Along with the JSON and XML conversion, the API supports many other [back and forth conversions](https://docs.groupdocs.com/conversion/net/supported-document-formats/) like word-processing documents, presentations, eBooks, JPG, PNG, WebP, and many more. You can see the details on the documentation.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/conversion) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert JSON to XML in C# {#json-to-xml}

Both the JSON and XML formats are commonly used in web-based applications to transmit data. These are structured, human-readable, hierarchical formats to store and exchange data.

The following steps guide you to convert the JSON data into XML format using .NET API.

*   Load the JSON data file using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Use the [DataConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/dataconvertoptions) to set the conversion format to XML.
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method of Converter class to transform the JSON Data into XML format

The following code converts the JSON data into XML format using C#.

{{< gist GroupDocsGists d7223aa52bb2ff2656761887bd65a9ab "ConvertJsonToXml.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To conclude, you have learned the conversion of JSON data to XML format within your .NET applications using C#. You can learn more about the .NET Conversion Automation API using the [documentation](https://docs.groupdocs.com/conversion/net/), or by quickly experiencing the examples available on [GitHub](https://github.com/groupdocs-conversion). Contact us for any query via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert JSON and CSV using C#](https://blog.groupdocs.com/2021/06/18/convert-json-and-csv-in-csharp/)
*   [Convert Excel and CSV using C#](https://blog.groupdocs.com/2021/08/18/convert-excel-xls-xlsx-and-csv-in-csharp/)




