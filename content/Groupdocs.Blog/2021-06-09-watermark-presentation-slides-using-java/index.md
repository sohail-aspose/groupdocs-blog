---
title: 'Watermark Presentation Slides using Java'
date: Wed, 09 Jun 2021 17:36:49 +0000
draft: false
url: /2021/06/09/watermark-presentation-slides-using-java/
author: 'Shoaib Khan'
summary: 'For the protection of the documents and presentations from illegal use, we can use watermarking. In this article, we will learn to programmatically apply text and image-based watermarks to the presentations or specific slides of a presentation in Java. In another post, we have discussed [applying watermarks to presentations using C#](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/).'
tags: ['Add Watermark to Presentation in Java', 'Image Watermark to PPT in Java', 'Text Watermark to PPT in Java', 'Watermark PPT in Java', 'Watermark PPTX in Java']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/apply-watermarks-to-presentations-in-java.jpg" alt="Apply Watermark to Presentation in Java">}}


For the protection of the documents and presentations from illegal use, we can use watermarking. In this article, we will learn to programmatically apply text and image-based watermarks to the presentations or specific slides of a presentation in Java. In another post, we have discussed [applying watermarks to presentations using C#](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/).

The following topics will be covered below:

*   [Java Watermarking API](#java-watermarking-api)
*   [Add text watermarks to presentation slides](#text-watermark-to-slides)
*   [Add image watermarks to presentation slides](#image-watermark-to-slides)

## Java Watermarking API for Presentations {#java-watermarking-api}

[GroupDocs.Watermark](https://products.groupdocs.com/watermark/) provides the Java API for watermarking, which allows adding text and image watermarks to the presentations within your application.

Alongside the presentations, the API supports adding, removing, and extracting watermarks from word-processing documents, spreadsheets, email messages, PDF files, images, and many other formats.

Among presentation file formats, it supports [PPT](https://docs.fileformat.com/presentation/ppt/), [PPTX](https://docs.fileformat.com/presentation/pptx/), [PPS](https://docs.fileformat.com/presentation/pps/), [PPTM](https://docs.fileformat.com/presentation/pptm/), [PPSX](https://docs.fileformat.com/presentation/ppsx/), and others. From the [documentation](https://docs.groupdocs.com/watermark/java/), you may further check the features and [supported file formats](https://docs.groupdocs.com/watermark/java/supported-document-formats/).

### Download and Configure

You can get the watermarking library from the [downloads section](https://downloads.groupdocs.com/watermark). For Maven-based Java applications, just add the following pom.xml configuration. Afterward, you can try watermarking examples of this article as well as many more examples from [GitHub](https://github.com/groupdocs-watermark). For the details, you may visit the [API Reference](https://apireference.groupdocs.com/conversion/java).

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-watermark</artifactId>
        <version>21.3</version> 
</dependency>
```

## Add Text Watermark to Presentation Slides in Java {#text-watermark-to-slides}

Using the API, you can apply customizations while adding text to presentation slides as a watermark. The following steps show how to apply watermark to presentations within the Java application.

*   Load the presentation using [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker).
*   Set watermark text and style using [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark).
*   Set watermark properties like size, location, opacity, rotation, and color.
*   Provide the slide index on which to apply the watermark. _(Optional)_
*   Add the formatted text watermark using the [add](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) method.
*   Save the watermarked presentation by calling the [save](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.io.OutputStream)) method.

The following code sample shows how to add a text watermark in PPT or PPTX on all the slides with rotation using Java.

{{< gist GroupDocsGists 9a6c523f3245fc7029a35217c15a1b97 "TextWatermarkToPresentation.java" >}}

If the slide index is not set, the watermark will be applied to all the slides of the presentation by default. The above code also shows how to mention the slide index. The following is the output with a text watermark on all the slides of the PPTX presentation.



{{< figure align=center src="images/text-watermark-to-slide-in-Java.png" alt="Text Watermark to Presentation Slide">}}


## Add Image Watermark to PPT Slides using Java {#image-watermark-to-slides}

You can add image watermarks on the presentation files as well with a similar approach. Just use the [ImageWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/ImageWatermark) class instead of the TextWatermark.

The following steps guide how to add image watermark to presentation slides within your Java applications.

*   Load the presentation file using [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker).
*   Load the image, logo, or photo using [ImageWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/ImageWatermark). It will be used as an image watermark.
*   Set image watermark properties like rotation, size, opacity, color, and position.
*   Set the slide index on which the watermark will be applied.
*   Add the image watermark to the presentation using [add](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) method.
*   Save the presentation with the image watermark using [save](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String,%20com.groupdocs.watermark.options.SaveOptions)) method.

The following code sample adds an image watermark to the second slide of the PPTX presentation in Java.

{{< gist GroupDocsGists 9a6c523f3245fc7029a35217c15a1b97 "ImageWatermarkToPresentation.java" >}}

The following is the output of the code with an image watermark only on the second slide of the PPT/PPTX.



{{< figure align=center src="images/image-watermark-to-slide-in-Java.png" alt="Image Watermark to Presentation Slide">}}


## Get a Free API License {#Get-a-Free-API-License}

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you have learned how to add watermarks to presentations in Java. To be more precise, we discussed how to insert text watermarks as well as image watermarks in presentations within Java-based applications. You can apply watermarks to all the slides as well as to any specific slide of the presentations.

Learn more about the API using [documentation](https://docs.groupdocs.com/watermark/). Examples are available at [GitHub](https://github.com/groupdocs-watermark). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Watermark Excel Sheets in Java](https://blog.groupdocs.com/2021/11/10/watermark-excel-sheets-in-java/)
*   [Add Watermark to Images and Photos in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)
*   [Find and Remove Watermarks from Documents in Java](https://blog.groupdocs.com/2020/11/30/find-and-remove-watermarks-from-documents-in-java/)
*   [Watermark Presentation Slides using C#](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/)




