---
title: 'Strikethrough Text in Documents using Java'
date: Mon, 06 Dec 2021 07:19:00 +0000
draft: false
url: /2021/12/06/strikethrough-text-in-documents-using-java/
author: 'Shoaib Khan'
summary: 'Probably you have some content that is no more valid. Let’s cross it out. Crossing out is one of the ways, used to highlight the invalid content within the documents. In order to automate the cross-out within the applications, this article shows how to strikethrough text in documents in Java.

The following topics are discussed in this article.

*   Java API for Strikethrough Annotations
*   How to Strikeout Text in Documents'
tags: ['Cross out Text', 'Cross out Text in Java', 'Strike through Text in Java', 'Strikeout Text', 'Strikethrough Text']
categories: ['GroupDocs.Annotation Product Family']
---



{{< figure align=center src="images/strikethrough-text-using-java.jpg" alt="StrikeThrough Text using Java">}}


Probably you have some content that is no more valid. Let's cross it out. Crossing out is one of the ways, used to highlight the invalid content within the documents. In order to automate the cross-out within the applications, this article shows **how to strikethrough text in documents in Java**.

The following topics are discussed in this article.

*   [Java API for Strikethrough Annotations](#strikethrough-text-java-api)
*   [How to Strikeout Text in Documents](#how-to-strikethrough-text-using-java)

## Java API to Strikethrough Text {#strikethrough-text-java-api}

[GroupDocs.Annotation](https://products.groupdocs.com/annotation/) showcases Java API that supports various annotations that can be applied to multiple documents and images. We will use it in the examples of this article to cross out the selected text within the documents.

You can download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/viewer) or use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs) configurations within your Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-annotation</artifactId>
        <version>21.7.2</version> 
</dependency>
```

## How to Strikethrough Text in Documents using Java {#how-to-strikethrough-text-using-java}

Let's cross out the area of the document that is not valid anymore. The following steps allow you to strike through the text within documents in Java.

*   Load the source document (PDF, Word, etc) using [Annotator](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator) class.
*   Create and define the strikethrough annotation using [StrikeoutAnnotation](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/StrikeoutAnnotation) class.
    *   Set the line color for strikeout.
    *   Set opacity, document page number.
    *   Define Coordinates and other properties.
*   Add the prepared strikeout annotation to the annotator using [add()](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#add(com.groupdocs.annotation.models.annotationmodels.AnnotationBase)) method.
*   Finally, save the annotated document using the [save()](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#save()) method.

Similarly, you can annotate Word documents, spreadsheets, presentations, PDF documents, web pages, email messages, and many other documents.

The following Java code example strikes out the selected text in a PDF document.

{{< gist GroupDocsGists d248b7146303cf285b8b51f6af40549b "StrikethroughText.java" >}}

## Get a Free API License

You can use [GroupDocs.Annotation for Java](https://products.groupdocs.com/annotation/java/) for free by [getting a temporary license](https://purchase.groupdocs.com/temporary-license).

## Conclusion

To conclude, we discussed programmatically adding the cross-out annotation to documents within Java applications. Additionally, you can strike out the text within PDF files, spreadsheets, presentations, and Word documents. Likewise, you can also use other annotations as you like.

Learn more about **GroupDocs.Annotation for Java** from its [documentation](https://docs.groupdocs.com/annotation/java/). Try building your own annotator for the [supported document formats](https://docs.groupdocs.com/annotation/java/supported-document-formats/). Feel free to contact us for queries via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Add or Remove Annotations from PDF files using Java](https://blog.groupdocs.com/2021/04/18/annotate-pdf-files-using-java/)
*   [Highlight PDF Content in Java](https://blog.groupdocs.com/2021/10/07/highlight-pdf-using-annotations-in-java/)
*   [Strikethrough Text in Documents using C#](https://blog.groupdocs.com/2021/12/18/strikethrough-text-in-documents-using-csharp/)




