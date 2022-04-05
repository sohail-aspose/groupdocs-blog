---
title: 'Convert Images to PDF in C#'
date: Wed, 19 May 2021 13:43:15 +0000
draft: false
url: /2021/05/19/convert-images-to-pdf-in-csharp/
author: 'Shoaib Khan'
summary: 'An Image can be converted to PDF to assure that the image will display correctly across devices without being altered. PDF images are ideal for printing and for storing images online when intended to be downloaded. PDF can hold as many images in one document so can be printed easily or saved as a catalog. This article will guide you to programmatically convert images like JPG, GIF, WebP, PNG to PDF in C# using .NET API for document and image conversion.

The following topics are covered briefly in this article:

*   Image Conversion .NET API
*   Convert JPG images to PDF
*   Convert PNG, GIF, BMP images to PDF
*   Image to PDF conversion with advance options

[Continue Reading ...](https://blog.groupdocs.com/2021/05/19/convert-images-to-pdf-in-csharp/)'
tags: ['Convert Images to PDF in CSharp', 'Convert JPG to PDF in CSharp', 'CSharp Image Conversion', 'JPG to PDF in CSharp', 'PNG to PDF in CSharp']
categories: ['GroupDocs.Conversion Product Family']
---

An Image can be converted to PDF to assure that the image is displayed correctly across devices without being altered. PDF images are ideal for printing and for storing images online when intended to be downloaded. PDF can hold as many images in one document so can be printed easily or saved as a catalog. This article will guide you to programmatically convert images like JPG, GIF, WebP, PNG to PDF in C# using .NET API for document and image conversion.

The following topics are covered briefly below:

*   [Image Conversion .NET API](#image-conversion-dotnet-api)
*   [Convert JPG images to PDF](#jpg-to-pdf)
*   [Convert PNG, GIF, BMP images to PDF](#png-gif-bmp-to-pdf)
*   [Image to PDF conversion with advance options](#advance-conversion)

## .NET API for Image Conversion {#image-conversion-dotnet-api}

I will use [GroupDocs.Conversion for .NET](https://products.groupdocs.com/conversion/net) library to convert images to PDF format. The library lets us convert a long list of image formats to PDF. Some of the supported ones are mentioned here. For the complete list, visit the [documentation](https://docs.groupdocs.com/conversion/net/supported-document-formats/#SupportedDocumentFormats-ConversionfromImageFiletoOtherDocumentformats).



{{< figure align=center src="images/convert-images-to-pdf-in-dotnet.jpg" alt="Convert Images to PDF using CSharp">}}


*   AI
*   BMP
*   CDR
*   DJVU
*   GIF
*   ICO
*   JPEG, JPG, JP2
*   PNG
*   SVGZ
*   TGA
*   TIF, TIFF
*   WEBP

Along with the images, the API allows the developers to convert Word documents, spreadsheets, presentations, eBooks, Visio documents, Microsoft Project files, PSD files, PDL, Email messages, and much more. Many examples are available at [GitHub](https://github.com/groupdocs-conversion) for the mentioned support.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/conversion/net) or get it from [NuGet](https://www.nuget.org/packages/GroupDocs.Conversion/).

```
Install-Package GroupDocs.Conversion
```

## Convert JPG to PDF in C# {#jpg-to-pdf}



{{< figure align=center src="images/Sample.jpg" alt="JPEG Image">}}


To simply convert your JPG images to PDF format, you can follow the below steps:

*   Load the JPG file using [Converter](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion/converter) class.
*   Instantiate [PdfConvertOptions](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions) class.
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to convert the JPG image into PDF and get it saved on the provided path.

The following source code shows how to convert a JPG image to PDF in C#.

{{< gist GroupDocsGists b19804d541cddbe28869fd02e067c42a "ConvertJPGToPDF.cs" >}}

## Convert PNG Images to PDF in C# {#png-gif-bmp-to-pdf}

If you want to convert a PNG image there will be no difference in the code. The following steps allow us to convert a PNG image to PDF using C#.

*   Load the PNG image file using [Converter](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion/converter) class.
*   Instantiate [PdfConvertOptions](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions) class.
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method to convert the provided image into PDF and get it saved on the provided path.

The following code shows how to convert a PNG image to PDF using C#.

{{< gist GroupDocsGists b19804d541cddbe28869fd02e067c42a "ConvertImageToPDF.cs" >}}

## Convert any Image to PDF

Similarly, you just have to provide your JPG, PNG, GIF, WebP, or any other image to the **Converter** class while loading. Also, there are many [conversion options](https://docs.groupdocs.com/conversion/net/convert-to-pdf-with-advanced-options/) while converting to PDF format.

## Convert Images to PDF in C# with Advanced Options {#advance-conversion}



{{< figure align=center src="images/AdvancedConversion-300x238.jpg" alt="Output Document After Conversion">}}


GroupDocs.Conversion provides [PdfConvertOptions](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions) to give us control over conversion results when converting Image to PDF. Some of the additional options are:

*   [Width](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/width) - Image width after conversion.
*   [Height](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/height) - Image height after conversion.
*   [MarginTop](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/margintop) - Page top margin after conversion.
*   [MarginBottom](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/marginbottom) - Page bottom margin after conversion.
*   [MarginLeft](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/marginleft) - Page left margin after conversion.
*   [MarginRight](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/marginright) - Page right margin after conversion.
*   [Rotate](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/rotate) - Page rotation. Available options are: None, On90, On180, On270

The following C# code sample uses these additional options and converts an image to PDF. It sets the height and width of the resultant image, sets the page margins, and also rotates the image at 180 degrees.

{{< gist GroupDocsGists b19804d541cddbe28869fd02e067c42a "ConvertImageToPdfAdv.cs" >}}

## Get a Free API License

You can use the API without evaluation limitations by requesting a [free temporary license](https://purchase.groupdocs.com/temporary-license).

## Conclusion

To conclude, we learned to convert images to PDF format using image conversion API for .NET. Specifically, we discussed how to programmatically convert JPG, PNG, WebP, and other images to PDF in C#. You can explore more about the image conversion API using the [documentation.](https://docs.groupdocs.com/conversion) For queries, reach us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert Excel Spreadsheets to PDF in C#](https://blog.groupdocs.com/2021/11/14/convert-excel-spreadsheets-to-pdf-using-csharp/)
*   [Convert CAD Drawings to PDF in C#](https://blog.groupdocs.com/2020/11/08/convert-cad-drawings-to-pdf-in-csharp/)
*   [](https://blog.groupdocs.com/2021/04/21/convert-images-to-pdf-in-java/)[Convert EML or MSG file to PDF in C#](https://blog.groupdocs.com/2019/12/06/convert-eml-or-msg-file-to-pdf-in-csharp/)




