---
title: 'Watermark PDF Files using C#'
date: Tue, 27 Jul 2021 14:34:00 +0000
draft: false
url: /2021/07/27/watermark-pdf-files-using-csharp/
author: 'Shoaib Khan'
summary: 'To protect your files from any illegal use or to apply branding to your documents, watermarks can be used . In this article, you will learn to programmatically add the watermarks to PDF files using C#. We will separately looking into adding watermark text and image watermarks.

The following topics are covered in this article:

*   .NET Watermarking API
*   Apply Text Watermark to PDF
*   Apply Image Watermark to PDF'
tags: ['.NET Watermarking API', 'Image Watermark in C#', 'Watermark in C#', 'Watermark PDF in C#', 'Watermark Text in C#']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/add-watermarks-to-pdf-in-csharp.jpg" alt="Apply Watermark to PDF in CSharp">}}


To protect your files from any illegal use or to apply branding to your documents, watermarks can be used. In this article, you will learn to programmatically add the watermarks to PDF files using C#. We will separately look into adding watermark text and image watermarks.

The following topics are covered below:

*   [.NET Watermarking API](#dotnet-watermarking-api)
*   [Apply Text Watermark to PDF](#text-watermark-to-pdf)
*   [Apply Image Watermark to PDF](#image-watermark-to-pdf)

## .NET Watermarking API for PDF files {#dotnet-watermarking-api}

[GroupDocs.Watermark](https://docs.groupdocs.com/watermark) provides .NET watermarking API that allows working with text as well as image watermarks within the PDF files. Along with the PDF files, the API allows adding, removing, and extraction of watermarks for word-processing documents, spreadsheets, presentations, email messages, images, Visio drawings, and many other formats. From the [documentation](https://docs.groupdocs.com/watermark/net), you may further check the features and [supported file formats](https://docs.groupdocs.com/watermark/net/supported-document-formats/).

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/watermark) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.watermark).

```
PM> Install-Package GroupDocs.Watermark
```

## Add Text Watermark to PDF using C# {#text-watermark-to-pdf}

The watermark text can be applied to PDF files on all the pages or any selective page. It can be added by inserting the formatted text on the required position.

The following steps show how to add watermark text to PDF files.

*   Load the PDF document using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker) class.
*   Initialize the text watermark using [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark) class.
*   Set the appearance by adding rotation angle, alignment, opacity, foreground and background colors, etc.
*   Set the targetted page index (_Optional_). If you do not set the index, the watermark will be applied to all pages by default.
*   Add the text watermark to the loaded PDF file.
*   Save the update file with watermark using the appropriate [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The source code shows how to add text watermark to PDF files using C#.

{{< gist GroupDocsGists 0fa75a5b1203743baf225f527098c3d3 "TextWatermarkToPDF.cs" >}}

The output of the above source code shows the text watermark on both the pages of the given PDF file.



{{< figure align=center src="images/add-text-watermark-to-pdf-in-csharp-1024x646.png" alt="Add Text Watermark to PDF using C#">}}


## Add Image Watermark to PDF using C# {#image-watermark-to-pdf}

Similarly, you can add images to the PDF file as we just added the text watermark.

The following steps show how to add an image to PDF files as watermarks.

*   Load the PDF document using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker) class.
*   Initialize the image watermark using [ImageWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/imagewatermark) class.
*   Set the appearance by adjusting the alignment, rotation, opacity, and other options.
*   Set the targetted page index. (Optional)
*   Add the image watermark to the PDF file.
*   Save the watermarked file using the appropriate [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The source code shows how to add image watermark to PDF files using C#.

{{< gist GroupDocsGists 0fa75a5b1203743baf225f527098c3d3 "ImageWatermarkToPDF.cs" >}}

The output of the above source code shows the image watermark on the second page of the given PDF file.



{{< figure align=center src="images/add-image-watermark-to-pdf-in-csharp-1024x625.png" alt="Image Watermark to PDF using C#">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To conclude, you learned how to add watermarks to PDF files using C#. We have seen adding watermark text as well as images on PDF files as watermarks. For more details or learning about the API, visit [documentation](https://docs.groupdocs.com/watermark/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Add Watermark to Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)
*   [Add Watermark to Presentation & Slides using C#](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/)
*   [Watermark Excel Sheets using C#](https://blog.groupdocs.com/2021/11/04/watermark-excel-sheets-using-csharp/)
*   [Password Protection to Lock & Unlock PDF Files in C#](https://blog.groupdocs.com/2021/11/17/password-protection-to-pdf-files-in-csharp/)




