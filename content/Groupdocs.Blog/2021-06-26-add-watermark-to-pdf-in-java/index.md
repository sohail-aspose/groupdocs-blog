---
title: 'Watermark PDF Files in Java'
date: Sat, 26 Jun 2021 09:48:16 +0000
draft: false
url: /2021/06/26/add-watermark-to-pdf-in-java/
author: 'Shoaib Khan'
summary: 'Whether you want to apply branding to your documents or you want to protect our files from any illegal use, the watermark does the job for you. In this article, you will learn to programmatically add the watermarks to your PDF files using Java.'
tags: ['Image Watermark PDF in Java', 'Text Watermark PDF in Java', 'Watermark in Java', 'Watermark PDF in Java', 'Watermarking Java API']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/apply-watermarks-to-pdf-in-java.jpg" alt="Apply Watermark to PDF in Java">}}


Whether you want to apply branding to your documents or you want to protect the files from any illegal use, the watermark does the job for you. In this article, you will learn to programmatically add the watermarks to your PDF files using Java.

The following topics are covered below:

*   [Java Watermarking API](#java-watermarking-api)
*   [Apply Text Watermark to PDF](#text-watermark-to-pdf)
*   [Apply Image Watermark to PDF](#image-watermark-to-pdf)

## Watermarking API for Java {#java-watermarking-api}

[GroupDocs.Watermark for Java](https://products.groupdocs.com/watermark/java) is a watermarking API that allows working with text and image watermarks within the PDF files. Along with the PDF files, the API allows adding, removing, and extraction of watermarks for word-processing documents, spreadsheets, presentations, email messages, images, Visio drawings, and many other formats. From the [documentation](https://docs.groupdocs.com/watermark/java/), you may further check the features and [supported file formats](https://docs.groupdocs.com/watermark/java/supported-document-formats/).

### Download and Configure

Get the PDF watermarking library from the [downloads](https://downloads.groupdocs.com/comparison/java) section. For Maven-based Java applications, add the following configuration within pom.xml. Later, you can try the examples of this article as well as many more from [GitHub](https://github.com/groupdocs-comparison). For the details, you may also visit the [API Reference](https://apireference.groupdocs.com/comparison/java).

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

## Add Text Watermark to PDF using Java {#text-watermark-to-pdf}

The text watermark can be applied to PDF files by adding the formatted text on either all the pages or any selective page on the set location.

The following steps show how to add text to PDF files as watermark.

*   Load the PDF document using [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker) class.
*   Initialize the text watermark using [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark) class.
*   Set the appearance by changing rotation angle, x-y positions, opacity, foreground and background colors, etc.
*   Set the targetted page index (Optional). If you do not set the index, the watermark will be applied to all pages by default.
*   Add the text watermark to Watermarker.
*   Save the watermarked file using the appropriate [save](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.io.OutputStream)) method.

The source code shows how to add text watermark to PDF files in Java.

{{< gist GroupDocsGists bd37f51efdd22e78fa9ff7e572060585 "TextWatermarkToPDF.java" >}}

The output of the above source code shows the text watermark on both the pages of the given PDF file.



{{< figure align=center src="images/text-watermark-to-pdf-in-java-1024x585.png" alt="Text Watermark to PDF">}}


## Add Image Watermark to PDF using Java {#image-watermark-to-pdf}

Similarly, you can add images to any PDF file at any location just like the text watermark options.

The following steps show how to add image to PDF files as watermark.

*   Load the PDF document using [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker) class.
*   Initialize the image watermark using [ImageWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/ImageWatermark) class.
*   Set the appearance by adjusting the rotation angle, x-y positions, opacity, and other options.
*   Set the targetted page index. (Optional)
*   Add the image watermark to Watermarker.
*   Save the watermarked file using the appropriate [save](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.io.OutputStream)) method.

The source code shows how to add image watermark to PDF files using Java.

{{< gist GroupDocsGists bd37f51efdd22e78fa9ff7e572060585 "ImageWatermarkToPDF.java" >}}

The output of the above source code shows the image watermark on the second page of the given PDF file.



{{< figure align=center src="images/image-watermark-to-pdf-in-java-1024x585.png" alt="Image Watermark to PDF">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, you learned to apply watermarks to PDF files using Java. We discussed adding text as well as images on PDF files as watermarks. For more details or learning about the API, visit [documentation](https://docs.groupdocs.com/watermark/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Add Watermark to Images in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)
*   [Watermark Excel Sheets in Java](https://blog.groupdocs.com/2021/11/10/watermark-excel-sheets-in-java/)
*   [Add Watermark to Presentations in Java](https://blog.groupdocs.com/2021/06/09/watermark-presentation-slides-using-java/)




