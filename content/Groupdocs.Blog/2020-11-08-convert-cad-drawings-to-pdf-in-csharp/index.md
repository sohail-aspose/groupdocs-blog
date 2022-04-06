---
title: 'Convert CAD Drawings to PDF in C#'
date: Sun, 08 Nov 2020 04:03:43 +0000
draft: false
url: /2020/11/08/convert-cad-drawings-to-pdf-in-csharp/
author: 'Shoaib Khan'
summary: 'Today, we will learn how to programmatically convert the CAD drawings to PDF format in C#. Previously, in an [earlier post](https://blog.groupdocs.com/2020/10/31/convert-cad-drawings-to-pdf-in-java/), we did the same but in Java. We looked to convert the DWG, DGN, and DWF files into PDF document with the code example. Let us do it in C# using the document conversion API for .NET.'
tags: ['convert cad to pdf', 'convert cad to pdf in csharp', 'convert dgn to pdf in csharp', 'convert dwf to pdf in csharp', 'convert dwg to pdf in csharp', ]
categories: ['GroupDocs.Conversion Product Family']
---

Today, we will learn how to programmatically convert the CAD drawings to PDF format in C#. Previously, in an [earlier post](https://blog.groupdocs.com/2020/10/31/convert-cad-drawings-to-pdf-in-java/), we did the same but in Java. We looked to convert the DWG, DGN, and DWF files into PDF documents with the code example. Let's do it in C# using the document conversion API for .NET.



{{< figure align=center src="images/convert-cad-drawings-to-pdf-using-dotnet.png" alt="Convert CAD Drawings to PDF in .NET">}}


The following topics will be covered in this article:

*   [C# API to Convert CAD Drawings](#cad-conversion-java-lib)
*   [Converting CAD Drawings (DWG, DWF, DGN) to PDF in C#](#convert-cad-dwg-dwf-dgn-to-pdf-in-java)

## C# API to Convert CAD Drawings {#cad-conversion-dotnet-lib}



{{< figure align=center src="images/groupdocs-conversion-net.png" alt="Convert Documents and Images using .NET">}}


[GroupDocs.Conversion for .NET](https://products.groupdocs.com/conversion/net) is the advanced conversion API for documents and images within any .NET application. It supports many file formats that include word-processing documents, spreadsheets, presentations, images, CAD drawings, and many more.

This article will be using GroupDocs.Conversion for .NET API for the **conversion of CAD drawings to PDF in C#**. You may [download](https://downloads.groupdocs.com/conversion/net) the DLL or get it installed using [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert CAD Drawings (DWG, DWF, DGN) to PDF in C# {#convert-cad-dwg-dwf-dgn-to-pdf-in-java}

The following steps will allow easy conversion of CAD drawings with a lot of options into a personalized PDF file.

*   **Load** CAD drawing.
*   Specify **layouts** and **options**.
*   **Convert** CAD with options to PDF.

### Load CAD Drawings

Load the CAD file using the [CadLoadOptions](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion.options.load/CadLoadOptions) class.

```
CadLoadOptions loadOptions =  new CadLoadOptions();
```

### Specify Layouts and Other options

You can specify certain [properties](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.load/cadloadoptions/properties/index) while loading CAD files. These properties include **layout names**, **width**, **height**, and **format**. Specifying layout names will allow you to convert only the mentioned layout.

```
Contracts.Func<LoadOptions> getLoadOptions = () => new CadLoadOptions
{
    LayoutNames = new \[\]{ "Layout1", "Layout3" },
    Width = 1920,
    Height = 1080
};
```

### Convert CAD Drawings - DWG, DWF to PDF in C#

Now using the Convert method of the Converter class, DWG or DWF files can be easily converted to PDF format using the set options.

```
using (Converter converter = new Converter("with\_layers\_and\_layouts.dwf", getLoadOptions))
{
    PdfConvertOptions options = new PdfConvertOptions();
    converter.Convert("converted.pdf", options);
}
```

### Complete Code

Here is the complete C# code, that you can use to convert DWG or DWF files into PDF by using the steps i.e. **Load** -> Specify **Layout and Options** -> **Convert**.

{{< gist GroupDocsGists f1e0ef5d80ba4f8bb44aa96085fb932b "ConvertCadToPDF.cs" >}}

There are many other customization options for the resultant PDF format that gives control over the output result while converting any document to the PDF format. You may have a look at these advanced options in the following documentation article.

[Convert to PDF with Advance Options in .NET](https://docs.groupdocs.com/conversion/net/convert-to-pdf-with-advanced-options/)

With a minor change, we can convert other CAD files like DGN and DWG files accordingly. We just have to provide the right filename and its format in the above code. For a file format that does not support layouts, we will not set **LayoutNames**. For such little modifications, you may visit the [documentation](https://docs.groupdocs.com/conversion/net/).

## Conclusion

I hope you are now confident with the conversion of CAD files like DWG, DGN, and DWF to PDF in C# using the GroupDocs.Conversion in your .NET as well as Java applications. You can now build your own conversion applications using any platform just like [free apps](https://products.groupdocs.app/conversion/total) available @ www.groupdocs.app.

You may contact the **Free Support Team for any further queries**, which is always available to help you on the [forum](https://forum.groupdocs.com/c/conversion).

## Related Articles

*   [Convert CAD Drawings to PDF in Java](https://blog.groupdocs.com/2020/10/31/convert-cad-drawings-to-pdf-in-java/)
*   [Excel Spreadsheets to PDF using C#](https://blog.groupdocs.com/2021/11/14/convert-excel-spreadsheets-to-pdf-using-csharp/)
*   [Load CAD documents](https://docs.groupdocs.com/conversion/net/load-cad-document-with-options/)
*   [Convert documents, and Images to PDF](https://docs.groupdocs.com/conversion/net/convert/pdf/)




