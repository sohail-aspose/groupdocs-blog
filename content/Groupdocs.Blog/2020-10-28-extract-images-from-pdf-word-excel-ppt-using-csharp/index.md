---
title: 'Extract Images from Documents using C#'
date: Wed, 28 Oct 2020 18:27:00 +0000
draft: false
url: /2020/10/28/extract-images-from-pdf-word-excel-ppt-using-csharp/
author: 'Shoaib Khan'
summary: 'In this article, we will be learning to **programmatically extract images from PDF, Excel, PowerPoint, and Word documents in a C#** application using document parsing .NET API. [GroupDocs.Parser for .NET](https://products.groupdocs.com/parser/net) is document parsing and data extraction .NET API. It supports **document parsing** and **extraction of images, text,** and **metadata** from **word-processing documents**, **spreadsheets**, **presentations, archives,** and **email** documents.'
tags: ['csharp parser', 'Dcoument Parsing API', 'extract images from PDF in csharp', 'extract images in csharp', 'Image extractor']
categories: ['GroupDocs.Parser Product Family']
---

In the [previous post](https://blog.groupdocs.com/2020/10/27/extract-images-from-pdf-word-excel-ppt-using-java/), we discussed how to extract images from documents in Java. Today, we will be looking to achieve the same objective using C#. No worries if you have not visited the last post. In this article, we will be learning to **programmatically extract images from PDF, Excel, PowerPoint, and Word documents in a C#** application using document parsing .NET API.



{{< figure align=center src="images/extract-images-from-documents-in-csharp-dotnet.png" alt="Extract Images from Documents in .NET">}}


Following topics will be covered here:

*   [Image, Text, and Metadata Extraction .NET API](#image-extraction-dotnet-api)
*   [Image Extraction from PDF documents](#extract-images-from-pdf-in-csharp)
*   [Extract Images from Word, Excel, PowerPoint documents](#extract-images-from-word-excel-ppt-in-csharp)
*   [Extract Image from Specific Page](#extract-images-from-specific-page-in-csharp)
*   [Supported Formats for Image Extraction](#supported-formats-for-image-extraction)

## Image, Text, and Metadata Extraction .NET API {#image-extraction-dotnet-api}



{{< figure align=center src="images/groupdocs-parser-net.png" alt="Parse Documents and Extract Data in .NET">}}


[GroupDocs.Parser for .NET](https://products.groupdocs.com/parser/net) is document parsing and data extraction .NET API. It supports **document parsing** and **extraction of images, text,** and **metadata** from **word-processing documents**, **spreadsheets**, **presentations, archives,** and **email** documents. At the end of the article, document formats are [mentioned](#supported-formats-for-image-extraction) that are supported by the API for image extraction.

In this article, we will use this API, so I would recommend to [download](https://downloads.groupdocs.com/parser/net) its binaries or install the API from [NuGet](https://www.nuget.org/packages/GroupDocs.Parser/) to prepare the environment.

## Extract Images from PDF Documents in C# {#extract-images-from-pdf-in-csharp}



{{< figure align=center src="images/PDF-with-Images.png" alt="PDF Document to Extract Images">}}


You can easily retrieve all the images from any PDF document by following these simple steps.

1.  Instantiate the [Parser](https://apireference.groupdocs.com/net/parser/groupdocs.parser/parser) class object with the source document.
2.  Call [GetImages](https://apireference.groupdocs.com/net/parser/groupdocs.parser/parser/methods/getimages) method of **Parser** class to get the collection of all the images in [PageImageArea](https://apireference.groupdocs.com/net/parser/groupdocs.parser.data/pageimagearea) objects.
3.  Iterate over **PageImageArea** to get every image.
4.  Save images on the disk using the [Save](https://apireference.groupdocs.com/parser/net/groupdocs.parser.data.pageimagearea/save/methods/1) method of **PageImageArea**.

Extracted images can be saved in **BMP**, **GIF**, **JPEG**, **PNG**, and **WebP** formats. The complete code is shown below to demonstrate the whole steps.

{{< gist GroupDocsGists 3bc831b64a139c428dffdb138332128a "ExtractImagesFromDocument.cs" >}}



{{< figure align=center src="images/Extracted-Images-from-PDF-using-GroupDocs.Parser-for-Java.png" alt="Extracted Images from Document using GroupDocs.Parser">}}


## Extract Images from Word, Excel, PowerPoint Files in C# {#extract-images-from-word-excel-ppt-in-csharp}

Not restricted to just PDF format, we can take out all the images from word-processing documents, spreadsheets, presentations, with the unchanged code base. Just change the source document path with the file extension, your document will be parsed to extract and save all the images to the disk.

```
using (Parser parser = new Parser("path/document.docx")) // Word Document
// using (Parser parser = new Parser("path/document.xlsx")) // Excel Spreadhseet
// using (Parser parser = new Parser("path/document.pptx")) // Presentation
// using (Parser parser = new Parser("path/document.pdf")) // PDF Document
```

## Image Extraction from Specific Document Page in C# {#extract-images-from-specific-page-in-csharp}

If you want to extract images from a specific page of the document, it can be done easily using the below-mentioned steps and C# code.

*   Get the information about the document using the [GetDocumentInfo](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser/methods/getdocumentinfo) method.
*   From the document information, take out the total [PageCount](https://apireference.groupdocs.com/parser/net/groupdocs.parser.options/idocumentinfo/properties/pagecount) and other information.
*   Use [GetImages(pageIndex)](https://apireference.groupdocs.com/parser/net/groupdocs.parser.parser/getimages/methods/2) method and pass your target page index to it.
*   To save the retrieved images, traverse the images collection, and save the individual image using the [Save](https://apireference.groupdocs.com/parser/net/groupdocs.parser.data.pageimagearea/save/methods/1) method.

{{< gist GroupDocsGists 3bc831b64a139c428dffdb138332128a "ExtractImagesFromDocumentPage.cs" >}}

## Supported Formats for Image Extraction in C# {#supported-formats-for-image-extraction}

Following are the document formats that are supported by the _GroupDocs.Parser for .NET_ API for image extraction.

<figure class="wp-block-table is-style-stripes"><table><tbody><tr><td>**Word Processing Documents</strong></td><td>DOC, DOCX, DOCM, DOT, DOTX, DOTM, ODT, OTT, RTF</td></tr><tr><td><strong>Spreadsheets</strong></td><td>XLS, XLSX, XLSM, XLSB, XLT, XLTX, XLTM, ODS, OTS, XLA, XLAM, NUMBERS</td></tr><tr><td><strong>Presentations</strong></td><td>PPT, PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP</td></tr><tr><td><strong>Portable Documents</strong></td><td>PDF</td></tr><tr><td><strong>Emails</strong></td><td>EML, EMLX, MSG</td></tr><tr><td><strong>Archives**</td><td>ZIP</td></tr></tbody></table></figure>

## More about GroupDocs.Parser

*   [Documentation](https://docs.groupdocs.com/parser/)
*   [Source Code Examples](https://github.com/groupdocs-parser/)
*   [API Reference](https://apireference.groupdocs.com/parser)
*   Family ([On-Premise APIs](https://products.groupdocs.com/parser/family)| [Cloud APIs](https://products.groupdocs.cloud/parser/family) | [Free Online App](https://products.groupdocs.app/parser))

Let's talk some more @ [Free Support Forum](https://forum.groupdocs.com/c/parser)

## Related Articles

*   [Extract Images from Documents using Java](https://blog.groupdocs.com/2020/10/27/extract-images-from-pdf-word-excel-ppt-using-java/)
*   [Extract Images from Documents on the Cloud using Python](https://blog.groupdocs.cloud/2020/10/25/extract-images-from-word-excel-ppt-pdf-using-python/)




