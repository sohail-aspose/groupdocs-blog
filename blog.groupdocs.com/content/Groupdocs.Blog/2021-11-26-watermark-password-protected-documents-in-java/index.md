---
title: 'Watermark Password Protected Documents in Java'
date: Fri, 26 Nov 2021 09:36:00 +0000
draft: false
url: /2021/11/26/watermark-password-protected-documents-in-java/
author: 'Shoaib Khan'
summary: ''
tags: ['Document Watermarking', 'Watermark Protected Documents using Java', 'Watermark Protected Files', 'Watermark Protected Files using Java', 'watermark using java', 'watermarking API for Java']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/watermark-protected-files-using-java.jpg" alt="Watermark Protected Docs using Java">}}


Watermarks can be used to protect the content and claim ownership of your documents. Similarly, these can also be used for branding or labelling your documents as drafts. This article discusses **how to add watermarks to the password-protected files** in Java. We will add text, as well as image watermarks to the protected files using code examples.

The following topics are discussed here:

*   [Java API to Watermark Password Protected Files](#watermarking-java-api)
*   [Add Watermark to Protected Files using Java](#add-watermark-to-protected-files)
    *   [Insert Text Watermark](#text-watermark-to-protected-files)
    *   [Insert Image Watermark](#image-watermark-to-protected-files)

## Java API to Watermark Password Protected Files {#watermarking-java-api}

[GroupDocs.Watermark](https://products.groupdocs.com/watermark/) showcases [watermarking Java API that allows working with watermarks](https://products.groupdocs.com/watermark/java/) within your applications. We will use this API to insert text and image watermarks to the password-protected documents.

You can download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/watermark) or use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs) configurations within your Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>https://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-watermark</artifactId>
        <version>21.3</version> 
</dependency>
```

## Adding Watermark to Password-Protected Files using Java {#add-watermark-to-protected-files}

Just a few lines of code allow you to customize the watermark as needed and apply it to your files. Follow the following steps for adding both types of watermark.

*   **Load** the protected file.
*   **Apply** watermark.
*   **Save** the watermarked file.

Now, we will add text watermarks, and then image watermarks, one by one.

## Add Text Watermark to Protected Files in Java {#text-watermark-to-protected-files}

Text watermarks can be used to mention the documents as DRAFT or CONFIDENTIAL; or for similar purposes. The following steps show how to add text watermark to password-protected documents in Java.

*   Prepare the [loading option](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.options/LoadOptions) using the exsiting password.
*   Use the loading options to load the protected file with [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker) class.
*   Define the watermark using [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark) class.
*   Set the text, appearance, rotation, opacity, color, and other properties of watermark.
*   Add the watermark to the document using the [add()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) method.
*   Save the watermarked file using the [save()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String)) method.

The following Java code snippet inserts a text watermark to a protected PDF document.

{{< gist GroupDocsGists a2137cc50ad466d561e69947e0a9c99e "AddTextWatermarkToPasswordProtectedDocument.java" >}}

## Add Image Watermark to Protected Files in Java {#image-watermark-to-protected-files}

You can also insert any image or logo as a watermark. To add the image, use the **ImageWatermark** class. The following steps allow adding an image watermark to your password-protected documents in Java.

*   Prepare the [loading option](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.options/LoadOptions) for the protected file using the exsiting password.
*   Load the file using the [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker) class and **loading option**.
*   Load the image file using [ImageWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/ImageWatermark) class.
*   Set the watermark's appearance, alignment, coordinates, rotation, opacity, and other properties.
*   Now, add watermark to document using [add()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) method.
*   Finally, save the watermarked file using the [save()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String)) method.

The following Java code example inserts an image watermark to the protected PDF file.

{{< gist GroupDocsGists a2137cc50ad466d561e69947e0a9c99e "AddImageWatermarkToPasswordProtectedDocument.java" >}}

## Get a Free API License

You can use the APIs for free by [getting a temporary license](https://purchase.groupdocs.com/temporary-license).

## Conclusion

To sum up, we discussed adding text watermarks, as well as image watermarks to password-protected files within the Java applications. Further, we customized the appearance of watermarks when these are applied to the documents.

In a similar vein, you can insert watermarks to the specific **pages, slides, and sheets of documents**, **presentations**, and **workbooks** respectively.

See the [related articles](#releated-articles) for details and learn more from its [documentation](https://docs.groupdocs.com/watermark/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## Related Articles {#releated-articles}

*   [Find and **Remove Watermarks** from Documents in Java](https://blog.groupdocs.com/2020/11/30/find-and-remove-watermarks-from-documents-in-java/)
*   [Add Watermark to **Images** in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)
*   [Password Protect Presentations in Java](https://blog.groupdocs.com/2022/02/10/lock-unlock-ppt-pptx-files-with-password-in-java/)
*   [Add Watermark to **Presentation Slides** using Java](https://blog.groupdocs.com/2021/06/09/watermark-presentation-slides-using-java/)
*   [Watermark **PDF** Files in Java](https://blog.groupdocs.com/2021/06/26/add-watermark-to-pdf-in-java/)




