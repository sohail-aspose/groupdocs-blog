---
title: 'Add Watermark to Images in Java'
date: Tue, 15 Sep 2020 14:16:12 +0000
draft: false
url: /2020/09/15/add-watermark-to-images-in-java/
author: 'Shoaib Khan'
summary: 'In this article, we will learn to **add text and image watermarks to images using Java**. There can be two ways to add watermark to images. Either you want to add the watermark with the personalized text or add an image watermark over the source image. We will see both scenarios. Currently, in addition to the JPG and PNG, this Java API supports BMP, GIF, JP2, TIFF & WebP image formats for adding watermarks on it. We can also change the style, orientation, and appearance of the watermark text.'
tags: ['add text and image watermarks java', 'add text to images in Java', 'image watermarks in Java', 'text watermarks in Java']
categories: ['GroupDocs.Watermark Product Family']
---

Worried about how to programmatically write text on an image using Java? In this article, we will learn to **add text and image watermarks to images using Java**. Previously, we have already seen the same using C# in another [post](https://blog.groupdocs.com/2019/10/21/add-watermark-to-images-using-csharp-dotnet-api/).



{{< figure align=center src="images/text-watermark-on-png-using-java.png" alt="Add Text Watermark to PNG image using Java">}}


There can be two ways to add a watermark to images. Either you want to add the watermark with the personalized text or add an image watermark over the source image. We will see both scenarios.

*   [Insert **Text Watermark** to Images](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/#add-text-watermark-to-images-in-java)
*   [Insert **Image Watermark** to Images](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/#add-image-watermark-to-images-in-java)

## Java Text and Image Watermarking API

In the examples below, we will be using [GroupDocs.Watermark for Java](https://products.groupdocs.com/watermark/java) API for adding text and image-based watermarking of JPG and PNG images. It will be better if you [download](https://downloads.groupdocs.com/watermark/java) the watermark API from the downloads section or integrate it into your Maven-based applications with the configurations mentioned on the same page.

## Add Text to Images as Watermark using Java {#add-text-watermark-to-images-in-java}

By following the below-mentioned steps and java code we can quickly add text to any image file as a watermark. I have watermarked the following JPG and PNG images using the same steps and below-mentioned code.



{{< figure align=center src="images/text-watermark-on-jpg-using-java.jpg" alt="Add Text Watermark to JPG image using Java">}}


Currently, in addition to the shown **JPG** and **PNG**, this Java API also supports **BMP, GIF, JP2, TIFF & WebP** image formats for adding watermarks to it.

*   Instantiate the [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark) object with the personalized text and style.
*   Adjust the text watermark settings.
*   Instantiate the [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker) with the source image.
*   Insert the watermark to the image using the [add](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) method.
*   Save the output image using the [save](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String)) method.

Here is the Java source code that adds the text watermark to the JPG image. If we need to apply the watermark to an image other than JPG, no big change is required. Just provide that image with the extension to the _Watermarker_ and the _save_ method. That's it.

We can also change the **style**, **orientation**, and **appearance** of the watermark text.

{{< gist GroupDocsGists c22738afc8956064dc9c56f62af14622 "AddTextWatermarkToPNG.java" >}}

## Insert Image Watermark on Images using Java {#add-image-watermark-to-images-in-java}



{{< figure align=center src="images/image-watermark-on-jpg-image-using-java.jpg" alt="Add Image Watermark to JPG image using Java">}}


Instead of adding text to an image, we can also add an image as a watermark on the source image. Follow the similar steps mentioned above but now you must use the **[ImageWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/ImageWatermark)** class instead of _TextWatermark_ used earlier to add text over the JPG and PNG images.

This [image](https://blog.groupdocs.com/wp-content/uploads/sites/4/2020/09/image-watermark-on-jpg-image-using-java.jpg) is created using the below mentioned Java source code and shows how we can add a PNG image watermark over the source JPG image:

{{< gist GroupDocsGists 0760dbd15da12362fa4e2f12cee2a073 "AddImageWatermarkToImage.java" >}}

## Conclusion

We have seen how to add text and image as a watermark on any image programmatically using Java. Furthermore, we change the text style and orientation of the watermark text.

You may explore the [documentation](https://docs.groupdocs.com/watermark/java/) for many more features of GroupDocs.Watermark for Java. For any ambiguity, you can directly contact the [free support](https://forum.groupdocs.com/c/watermark) for quick response,

## See Also

*   [Add Watermark to Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)
*   [Watermark Excel Sheets in Java](https://blog.groupdocs.com/2021/11/10/watermark-excel-sheets-in-java/)
*   [Remove Watermarks from Documents in Java](https://blog.groupdocs.com/2020/11/30/find-and-remove-watermarks-from-documents-in-java/)




