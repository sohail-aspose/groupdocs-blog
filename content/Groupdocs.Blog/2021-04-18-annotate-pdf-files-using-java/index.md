---
title: 'Add or Remove Annotations from PDF files using Java'
date: Sun, 18 Apr 2021 05:20:00 +0000
draft: false
url: /2021/04/18/annotate-pdf-files-using-java/
author: 'Shoaib Khan'
summary: 'There was a time when we used to discuss document content and feedback in long email threads with multiple attachments and different file versions. Now we can simply use annotations to markup the document with messages and replies and send it. In this article, you will learn how to programmatically annotate PDF documents in Java with your application.'
tags: ['add annotations in PDF using Java', 'Annotate PDF in Java', 'Remove annotations from PDF in Java']
categories: ['GroupDocs.Annotation Product Family']
---

There was a time when we used to discuss document content and feedback in long email threads with multiple attachments and different file versions. Now we can simply use annotations to markup the document with messages and replies and send it. In this article, you will learn how to programmatically annotate PDF documents in Java with your application. Additionally, we will see how to remove annotations from PDF files using the same Java API.

The following are the topics discussed briefly below:

*   [Java API to Work with Annotations in PDF](#pdf-annotation-java-api)
*   [Add Annotations to PDF in Java](#add-annotations-to-pdf-in-java)
    *   [Arrow annotation in PDF](#add-arrow-annotation-to-pdf-in-java)
    *   [Rectangle annotation in PDF](#rectangle-area-annotation-to-pdf-in-java)
    *   [Ellipse or Oval annotation in PDF](#oval-ellipse-annotation-to-pdf-in-java)
    *   [Distance annotation in PDF](#distance-annotation-to-pdf-in-java)
*   [Remove Annotations from PDF in Java](#remove-annotations-from-pdf-in-java)

## PDF Annotator Java API {#pdf-annotation-java-api}

To deal with annotations of your document and images within your Java applications, GroupDocs provides [GroupDocs.Annotation for Java](https://products.groupdocs.com/annotation/java). Using the API, you can add, remove, and extract annotations from **word-processing** documents, **spreadsheets**, **presentations**, **images**, **email messages**, Visio **drawings**, some **AutoCAD**, and **digital imaging formats** like **DICOM**. Furthermore, the API allows annotating PDF files. You may have a look at the documentation to know about the long list of [supported document formats for annotation](https://docs.groupdocs.com/annotation/java/supported-document-formats/).

### Download and Configure

[Get the annotation library ](https://downloads.groupdocs.com/annotation/java)from downloads or just add the following pom.xml configuration in your Maven-based Java applications to try the examples of this article as well the many more example available on [GitHub](https://github.com/groupdocs-annotation). For the details, you may visit the [API Reference](https://apireference.groupdocs.com/annotation/java).

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-annotation</artifactId>
        <version>20.2</version> 
</dependency>
```

## Add Annotations to PDF in Java {#add-annotations-to-pdf-in-java}

Let's quickly jump to add some of the different kinds of annotations to the PDF document. As there are many different types of annotation, we may not cover all in this article. I will just mention them, and you may [learn about each annotation individually](https://docs.groupdocs.com/annotation/java/add-annotation-to-the-document/).

*   Area / Rectangle annotation
*   Arrow
*   Distance
*   Ellipse
*   Highlight
*   Link
*   Point
*   Polyline

*   Replacement
*   Resource Redaction
*   Strikeout
*   Text Field
*   Text Redaction
*   Underline
*   Watermark

Let's start adding some of these in a PDF document.

## Add Arrow Annotation to PDF using Java {#add-arrow-annotation-to-pdf-in-java}

The following are the steps to add arrow annotation to a PDF document.



{{< figure align=center src="images/arrow-annotation.jpg" alt="Arrow Annotation">}}


*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator) class.
*   Initialize arrow annotation using [ArrowAnnotation](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/ArrowAnnotation) class.
*   Set the position and size of the arrow using [setBox](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/ArrowAnnotation#setBox(com.groupdocs.annotation.models.Rectangle)) method of ArrowAnnotation.
*   Add the created arrow annotation to the Annotator object.
*   Save the annotated PDF by providing the path using the [save](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#save(java.lang.String)) method.

The following code sample shows how to add arrow annotation to a PDF document using Java.

{{< gist GroupDocsGists 82c10a1efcae60359901cecbda8f6c20 "AddArrowAnnotationToPDF.java" >}}

## Insert Rectangle or Area Annotation to PDF using Java {#rectangle-area-annotation-to-pdf-in-java}

You can customize any annotation while adding it to the document. The following are the steps to add rectangle or area annotation to a PDF document with little more customizations. It is similar to adding Arrow annotation but uses **AreaAnnotation** class in place of **ArrowAnnotation**.

*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator) class.
*   Initialize rectangle annotation using [AreaAnnotation](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/AreaAnnotation) class.
*   Set the position and size of the rectangle using [setBox](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/ArrowAnnotation#setBox(com.groupdocs.annotation.models.Rectangle)) method of AreaAnnotation.
*   Set other properties like **color**, **background**, **opacity**, **style**, **pen width**, or even **messages**, and **time**.
*   Add the created rectangle annotation to the Annotator object.
*   Save the annotated PDF by providing the path using the [save](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#save(java.lang.String)) method.



{{< figure align=center src="images/rectangle-area-annotation.jpg" alt="Rectangle or Area Annotation">}}


The following code sample shows how to add rectangle/area annotation to a PDF document using Java.

{{< gist GroupDocsGists 82c10a1efcae60359901cecbda8f6c20 "AddRectangleAnnotationToPDF.java" >}}

## Add Oval or Ellipse Annotation to PDF using Java {#oval-ellipse-annotation-to-pdf-in-java}

The following are the steps to add oval annotation or ellipse annotation to a PDF document.



{{< figure align=center src="images/ellipses-annotation.jpg" alt="Ellipses or Oval Annotation">}}


*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator) class.
*   Initialize ellipse annotation using [EllipseAnnotation](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/EllipseAnnotation) class.
*   Set the position and size of the ellipse using [setBox](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/ArrowAnnotation#setBox(com.groupdocs.annotation.models.Rectangle)) method of EllipseAnnotation.
*   Add the created ellipse annotation to the Annotator object.
*   Save the annotated PDF by providing the path using the [save](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#save(java.lang.String)) method.

The following code sample shows how to add oval or ellipse annotation to a PDF document using Java.

{{< gist GroupDocsGists 82c10a1efcae60359901cecbda8f6c20 "AddOvalAnnotationToPDF.java" >}}

## Insert Distance Annotation to PDF using Java {#distance-annotation-to-pdf-in-java}



{{< figure align=center src="images/distance-annotation.jpg" alt="Distance Annotation">}}


You can also add the distance annotation to show the distance between two points. The following are the steps to add distance annotation to the PDF document.

*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator) class.
*   Initialize distance annotation using [DistanceAnnotation](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/DistanceAnnotation) class.
*   Set the size and position of the annotation using [setBox](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.models.annotationmodels/ArrowAnnotation#setBox(com.groupdocs.annotation.models.Rectangle)) method of DistanceAnnotation.
*   Add the created distance annotation to the Annotator object.
*   Save the annotated PDF by providing the path using the [save](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#save(java.lang.String)) method.

The following code sample shows how to add distance annotation to a PDF document using Java.

{{< gist GroupDocsGists 82c10a1efcae60359901cecbda8f6c20 "AddDistanceAnnotationToPDF.java" >}}

## Complete Code

To sum up, here is the Java code with the output showing all the added **annotations** and **messages** with **replies** using the mentioned Java code.



{{< figure align=center src="images/added-annotations-to-pdf.jpg" alt="Added Annotations to PDF">}}


The following code below adds, arrow, rectangle, ellipse, distance annotations, messages, and replies to a PDF file.

{{< gist GroupDocsGists 82c10a1efcae60359901cecbda8f6c20 "AddAnnotationsToPDF.java" >}}

## Remove Annotations from PDF in Java {#remove-annotations-from-pdf-in-java}

The following steps show how to remove all the annotations from PDF files in Java.

*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator) class.
*   Initialize saving Options using [SaveOptions](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation.options.export/SaveOptions) class.
*   Set the annotation types to None.
*   Save the PDF file having all the annotations removed, by providing the path using the [save](https://apireference.groupdocs.com/annotation/java/com.groupdocs.annotation/Annotator#save(java.lang.String)) method.

The following Java code removes annotations from a PDF file.

{{< gist GroupDocsGists 82c10a1efcae60359901cecbda8f6c20 "RemoveAnnotationsFromPDF.java" >}}

## Conclusion

In short, you have learned how to add annotations to PDF within Java applications. Further, you have seen how to remove all the annotations from any PDF file. Now, you should be confident to build your own document annotator Java application. It can support different types of annotations using GroupDocs.Annotation for Java.

For more details, options, and examples, you can visit the [documentation](https://docs.groupdocs.com/annotation/java/) and the [GitHub](https://github.com/groupdocs-annotation) repository. For further queries, contact the support on the [forum](https://forum.groupdocs.com/).

## See Also

*   [Add Watermark to Images in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)




