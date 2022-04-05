---
title: 'Watermark Password Protected Documents using C#'
date: Sat, 25 Dec 2021 07:54:23 +0000
draft: false
url: /2021/12/25/watermark-password-protected-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'Watermarking is one of the ways to protect your documents from illegal use; branding your files; mentioning your documents as drafts or confidential. In order to watermark your files programmatically, this article guides you on **how to add watermark to your password-protected files using C#**. We will separately look into adding text and image watermarks to the protected files.

The following topics are discussed in this article:

*   .NET API to Watermark Password Protected Files
*   Add Watermark to Protected Files using C#
    *   Apply Text Watermark
    *   Apply Image Watermark'
tags: ['Document Watermarking', 'Watermark Protected Documents using CSharp', 'Watermark Protected Files using CSharp', 'watermark using csharp', 'Watermarking API for .NET']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/watermark-protected-files-using-csharp.jpg" alt="Watermark Protected Docs using C#">}}


Watermarking is one of the ways to protect your documents from illegal use; branding your files; mentioning your documents as drafts or confidential. In order to watermark your files programmatically, this article guides you on **how to add watermark to your password-protected files using C#**. We will separately look into adding text and image watermarks to the protected files.

The following topics are discussed here:

*   [.NET API to Watermark Password Protected Files](#watermarking-dotnet-api)
*   [Add Watermark to Protected Files using C#](#add-watermark-to-protected-files)
    *   [Apply Text Watermark](#text-watermark-to-protected-file)
    *   [Apply Image Watermark](#image-watermark-to-protected-file)

## .NET API to Watermark Password Protected Files {#watermarking-dotnet-api}

[GroupDocs.Watermark](https://products.groupdocs.com/watermark/) provides a watermarking solution and showcases [.NET API that allows working with watermarks](https://products.groupdocs.com/watermark/net/) within .NET applications. I will use this API to add text and image watermarks to password-protected files.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/watermark) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.watermark).

```
PM> Install-Package GroupDocs.Watermark
```

## Adding Watermark to Password-Protected Files using C# {#add-watermark-to-protected-files}

It's quite simple; just a few lines of code allow you to put a watermark in your files. Just follow the following steps for adding either type of watermark.

*   **Load** the protected document/file.
*   **Apply** text/image watermark.
*   **Save** the watermarked file.

Let's separately see how to add text watermarks, and then image watermarks.

## Add Text Watermark to Protected Files using C# {#text-watermark-to-protected-file}

Text watermarks are most used to put the company name within documents; mention the document as DRAFT or CONFIDENTIAL; or any other similar reasons. The following steps guide how to insert text watermark to password-protected files using C#.

*   Prepare the [loading option](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.options/loadoptions) using exsiting password.
*   Load the protected file using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker) class and **loading option**.
*   Prepare the watermark using [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark) class.
*   Set the watermark's text, appearance, rotation, opacity, color, and other properties.
*   Add watermark to document using [Add()](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) method.
*   Save the watermarked file using the [Save()](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following C# code inserts a text watermark to a protected PDF document.

{{< gist GroupDocsGists 02f763046a5c3b45f722e88c0ead9029 "AddTextWatermarkToPasswordProtectedDocument.cs" >}}

## Add Image Watermark to Protected Files using C# {#image-watermark-to-protected-file}

If you want to insert your logo or some other image as a watermark, you can add it using the ImageWatermark class. The following steps allow you to add an image watermark to your password-protected documents using C#.

*   Prepare the [loading option](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.options/loadoptions) using exsiting password.
*   Load the protected file using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker) class and **loading option**.
*   Load the watermark image file using [ImageWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/imagewatermark) class.
*   Set the watermark's appearance, alignment, coordinates, rotation, opacity, and other properties.
*   Add watermark to document using [Add()](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) method.
*   Save the watermarked file using the [Save()](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following C# code inserts an image watermark to the protected MS Word DOCX document.

{{< gist GroupDocsGists 02f763046a5c3b45f722e88c0ead9029 "AddImageWatermarkToPasswordProtectedDocument.cs" >}}

## Get a Free API License

You can use the APIs for free by [getting a temporary license](https://purchase.groupdocs.com/temporary-license).

## Conclusion

To conclude, we learned to add text watermarks, as well as image watermarks to password-protected files within the .NET applications using C#. Further, we added a few customizations to the appearance of watermarks while adding.

Similarly, you can apply watermarks to the selective **pages of documents**, chosen **slides of the presentations**, and specific **sheets of workbooks** within your documents. See the [related articles](#releated-articles) for details.

To learn more about [GroupDocs.Watermark for .NET](https://products.groupdocs.com/watermark/net/), visit its [documentation](https://docs.groupdocs.com/watermark/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## Related Articles {#releated-articles}

*   [Find and **Remove Watermarks** from Documents in C#](https://blog.groupdocs.com/2020/11/27/find-and-remove-watermarks-from-documents-in-csharp/)
*   [Watermark **Excel Sheets** using C#](https://blog.groupdocs.com/2021/11/04/watermark-excel-sheets-using-csharp/)
*   [Watermark **PDF** Files using C#](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/)
*   [Add Watermark to **Presentation Slides** using C#](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/)
*   [Add Watermark to **Images** using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)




