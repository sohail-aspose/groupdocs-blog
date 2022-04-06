---
title: 'Add Watermark to Images using C#'
date: Sun, 20 Dec 2020 11:03:00 +0000
draft: false
url: /2020/12/20/add-watermark-to-images-using-csharp-dotnet/
author: 'Shoaib Khan'
summary: 'Let us see today, how to add watermarks to images. This helps you branding your official photography, and protects your pictures from any unauthorized use. This article will guide you to **programmatically add text and images watermarks to your image files using C#**. In an earlier post, we have seen the same to [add text and image based watermarks to images using Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/). After reading this article, it will not be difficult for you to add watermarks to **JPG/JPEG, PNG, WebP, GIF, TIFF, JP2, BMP** images using C# within your .NET application.'
tags: ['add watermark in csharp', 'how to add watermark in csharp', 'watermark dotnet api', 'watermark images in csharp']
categories: ['GroupDocs.Watermark Product Family']
---

Let's see today, how to add watermarks to images. This helps you brand your official photography, and protects your pictures from any unauthorized use. This article will guide you to **programmatically add text and image watermarks to your image files using C#**. In an earlier post, we have seen the same to [add text and image-based watermarks to images using Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/). After reading this article, it will not be difficult for you to add watermarks to **JPG/JPEG, PNG, WebP, GIF, TIFF, JP2, BMP** images using C# within your .NET application.

Let's now separately see, how we can easily add text and image-based watermarks on your pictures, photos, or image files in C# using the [.NET Watermarking API for documents and images](https://products.groupdocs.com/watermark/net).

*   [Add Text on Images as Watermark](#add-text-watermark-to-image-using-csharp)
*   [Insert Image Watermark to Images](#add-image-watermark-to-image-using-csharp)

## Text and Image Watermarking API for .NET {#mce_0}



{{< figure align=center src="images/groupdocs-watermark-net.png" alt="Watermark API for .NET - GroupDocs">}}


**GroupDocs.Watermark for .NET** is an API for adding watermarks to the images or documents of different file formats within .NET applications. It provides effective watermarking methods that allow you to add text watermarks as well as image watermarks that are hard to get automatically removed by other third-party tools.

From the [documentation](https://docs.groupdocs.com/watermark/net/), you may further check the features and [supported file formats](https://docs.groupdocs.com/watermark/net/supported-document-formats/).

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/watermark/net) or get it from [NuGet](https://www.nuget.org/packages/GroupDocs.Watermark/).

```
Install-Package GroupDocs.Watermark
```

## Add Text to Images as Watermark using C# {#add-text-watermark-to-image-using-csharp}



{{< figure align=center src="images/text-watermark-on-png-using-java.png" alt="Add Text Watermark to PNG image using Java and .NET">}}


The API allows you to add text to images as a watermark with many customizations. The following steps guide how we can apply watermark on our images files, photos, or pictures using C# within the .NET application.

1.  Load the Image using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker).
2.  Set the watermark text and style using [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark).
3.  Set other watermark properties like position, rotation, opacity, etc.
4.  Add the text watermark to the image using the [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) method.
5.  Save the output image with [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following C# code sample adds a text label on a JPG image as a watermark with some text rotation.

{{< gist GroupDocsGists c22738afc8956064dc9c56f62af14622 "AddTextWatermarkToJPG.cs" >}}

## Insert Image Watermark to Images using C# {#add-image-watermark-to-image-using-csharp}



{{< figure align=center src="images/image-watermark-on-jpg-image-using-java.jpg" alt="Add Image Watermark to JPG image using GroupDocs.Watermark">}}


Similarly, we can also add another image as a watermark on our source image files. For this, use **ImageWatermark** class and its properties to customize the watermark appearance.

*   Create [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker) class object to load the source image.
*   Prepare image watermark using [ImageWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/imagewatermark) class.
*   Set the watermark properties.
*   Add the image watermark on the source image using [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) method.
*   Save the output image using [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following C# code sample adds a PNG image on another PNG file as a watermark on the preferred location.

{{< gist GroupDocsGists 0760dbd15da12362fa4e2f12cee2a073 "AddImageWatermarkToImage.cs" >}}

## Conclusion

I am confident that you can now easily add a watermark to your image files using C#. Even you can build your own .NET application that supports watermarking the documents and images of various file formats.

You can have a [Free Temporary License](https://purchase.groupdocs.com/temporary-license) to experience every aspect of the product. Free support will be happy to get you out of any confusion and [resolve your watermark-related queries on the forum](https://forum.groupdocs.com/c/watermark).

## See Also

*   [Add Watermark to Excel Sheets using C#](https://blog.groupdocs.com/2021/11/04/watermark-excel-sheets-using-csharp/)
*   [Remove Watermark from Documents in C#](https://blog.groupdocs.com/2020/11/27/find-and-remove-watermarks-from-documents-in-csharp/)
*   [Add Watermark to Images in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)




