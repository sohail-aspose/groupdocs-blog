---
title: 'Add Watermark to Presentation Slides using C#'
date: Sat, 01 May 2021 04:00:00 +0000
draft: false
url: /2021/05/01/add-watermark-to-presentations-using-csharp/
author: 'Shoaib Khan'
summary: 'Watermarks are normally used to protect the documents from any unauthorized use. To protect your presentations and to claim ownership, today we will learn how to programmatically add text and image watermarks to the Microsoft PowerPoint presentations within .NET applications using C#. In a separate article, we have seen [applying watermarks to images in C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/).

The following topic are separately and briefly covered in this artile:

*   Add text watermarks to presentation slides.
*   Add image watermarks to presentation slides.

[Continue Reading ...](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/)'
tags: ['add watermark in csharp', 'add watermark to presentations in csharp', 'how to add watermark in csharp']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/apply-watermarks-to-presentations-in-csharp.jpg" alt="Apply Watermark to Presentation in C#">}}


Watermarks are normally used to protect the documents from any unauthorized use. To protect your presentations and to claim ownership, today we will learn how to programmatically add text and image watermarks to the Microsoft PowerPoint presentations within .NET applications using C#. In a separate article, we have seen [applying watermarks to images in C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/).

Let's quickly move to separately learn, how we can apply text and image-based watermarks to the whole presentation or specific slide using the [watermarking API for .NET applications](https://products.groupdocs.com/watermark/net).

*   [Add text watermarks to presentation slides](#text-watermark-to-slides-in-csharp).
*   [Add image watermarks to presentation slides.](#image-watermark-to-slides-in-csharp)

## Watermarking API for .NET

[GroupDocs.Watermark for .NET](https://products.groupdocs.com/watermark/net) is a watermarking API that allows adding text and image watermarks to the presentations and many other documents of different file formats within .NET applications. It provides watermarking methods that add watermarks that are hard to get automatically removed by other tools.

Along with the presentations, the API supports adding, removing, and extracting watermarks from word-processing documents, spreadsheets, email messages, PDF files, images, Visio drawings, and many other formats. Among presentation file formats, it supports PPT, PPTX, PPS, PPTM, PPSX, and others. From the [documentation](https://docs.groupdocs.com/watermark/net/), you may further check the features and [supported file formats](https://docs.groupdocs.com/watermark/net/supported-document-formats/).

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/watermark/net) or get it from [NuGet](https://www.nuget.org/packages/GroupDocs.Watermark/).

```
Install-Package GroupDocs.Watermark
```

## Add Text to Slides as Watermark using C# {#text-watermark-to-slides-in-csharp}

The API provides customizations to add text to presentations as watermark. The following steps guide you how to apply watermark on presentation files within .NET application.

*   Load the presentation using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker).
*   Set watermark text and style using [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark).
*   Set other properties like rotation, size, opacity, color, and position.
*   Provide the index of the slide to apply the watermark.
*   Add the formatted text watermark using [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) method.
*   Save the watermarked presentation using the [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following code sample adds a text label to the PPTX presentation as a watermark on the first slide with rotation using C#.

{{< gist GroupDocsGists c5637a7b8dd5d881e58e502c109ca4a0 "AddTextWatermarkToPresentation.cs" >}}

If you do not provide a slide index, the watermark will be added on all the slides by default. The above code shows how to mention the slide index, however, I have shown you the output with a text watermark on all the slides of the PPTX presentation.



{{< figure align=center src="images/text-watermark-to-slide.png" alt="Text Watermark to Presentation Slide">}}


## Insert Image Watermark to Slides using C# {#image-watermark-to-slides-in-csharp}

Likewise, you can add images on presentation files as watermark. You just have to use the [ImageWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/imagewatermark) class instead of the TextWatermark. The following are the steps to add image watermark to presentation slides within your .NET applications.

*   Load the presentation using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker).
*   Load the image file that will be used as a watermark using [ImageWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/imagewatermark).
*   Set image watermark properties like rotation, size, opacity, color, and position.
*   Set the slide index on which to apply the watermark.
*   Add the image watermark to the presentation using [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) method.
*   Save the watermarked presentation using the [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following code sample adds an image to the PPTX presentation as a watermark on the second slide using C#.

{{< gist GroupDocsGists c5637a7b8dd5d881e58e502c109ca4a0 "AddImageWatermarkToPresentation.cs" >}}

The following is the output of the above code with an image watermark only on the second slide of the PPTX presentation.



{{< figure align=center src="images/image-watermark-to-slide.jpg" alt="Image Watermark to Presentation Slide">}}


## Conclusion

To sum up, you have learned how to add text and image watermarks to your presentation slides using C#. Now you can build your own .NET application that supports text as well as image watermarks for the presentation files and specific slides of the presentation. Consult the documentation to [apply watermarks to various other document formats](https://docs.groupdocs.com/watermark/net/adding-watermarks/).

You can have a [Free Temporary License](https://purchase.groupdocs.com/temporary-license) to experience every aspect of the product. Free support will be happy to get you out of any confusion and [resolve your queries related to watermarks on the forum](https://forum.groupdocs.com/c/watermark).

## See Also

*   [Add Watermark to Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)
*   [Insert Watermark to Excel Workbooks using C#](https://blog.groupdocs.com/2021/11/04/watermark-excel-sheets-using-csharp/)
*   [Find and Remove Watermarks from Documents in C#](https://blog.groupdocs.com/2020/11/27/find-and-remove-watermarks-from-documents-in-csharp/)




