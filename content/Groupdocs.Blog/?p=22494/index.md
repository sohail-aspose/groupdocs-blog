---
title: 'Add or Remove Annotations or Markup PDF files using C#'
date: 
draft: true
url: /?p=22494
author: 'Shoaib Khan'
summary: ''
tags: ['Uncategorized']
---

Forget to discuss documents' content and feedbacks in long email threads. Simply use annotations to markup documents with messages and replies. In this article, you will learn how to programmatically add and remove annotations to markup PDF documents in C# with your .NET applications.

The following are the topics discussed briefly below:

*   .NET API for PDF Annotations
*   Add Annotations to PDF
    *   Arrow annotations
    *   Rectangle annotations
    *   Ellipse or Oval annotations
    *   Distance annotations
*   Remove Annotations from PDF

## .NET API for PDF Annotations and Markup {#block-ed11fda3-3781-494e-900a-e7a92046e50f}

[GroupDocs.Annotation](https://products.groupdocs.com/annotation/) provides the .NET API to work with the annotations for your documents and images within your .NET applications. The API allows you to add, remove, and extract annotations. Along with the PDF documents, it supports **word-processing** documents, **spreadsheets**, **presentations**, **images**, webpages, **email messages**, Visio **drawings**, some **AutoCAD**, and **digital imaging formats** like **DICOM** and much more. For complete list of [supported document formats for annotation](https://docs.groupdocs.com/annotation/net/supported-document-formats/), you can visit the documentation.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/annotation) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.annotation).

```
PM> Install-Package GroupDocs.Annotation
```

## Add Annotations to PDF in C# {#block-342e4669-e2f7-4fbb-bcca-1e7293c1b8e2}

Let's add some of the different kinds of annotations to the PDF document. There are many different types of annotation, so we will be covering only a few in this article. There are some of the supported annotation types, you may [learn about each annotation individually](https://docs.groupdocs.com/annotation/net/add-annotation-to-the-document/).

*   Area / Rectangle annotation
*   Arrow
*   Underline
*   Watermark
*   Distance
*   Strikeout
*   Text Field
*   Ellipse
*   Highlight
*   Link
*   Point
*   Polyline
*   Replacement
*   Resource Redaction
*   Text Redaction

## Add Arrow Annotation to PDF using C# {#block-34ff7799-9d51-438b-8ba0-df70239ae3ed}

The following are the steps to add arrow annotation to a PDF document in C#.



{{< figure align=center src="images/arrow-annotation.jpg" alt="Add Arrow Annotation Programmatically">}}


*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   Initialize arrow annotation with [ArrowAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/arrowannotation) class.
*   Adjust the position, size, page number of the arrow annotation.
*   Add the created arrow annotation using [Add](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/add/index) method.
*   Save the annotated PDF to the path using the [Save](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

The following code sample shows how to add an arrow annotation to a PDF document using C#.

<code>

## Insert Rectangle or Area Annotation to PDF using C# {#block-6c36bc81-4733-4e92-b0ec-5fd915c5316f}

Customizations can be done for any annotation while adding it to the document. The following are the steps to add rectangle or area annotation to a PDF document with some customizations. It is very similar to adding Arrow annotations but uses **AreaAnnotation** class this time.

*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   Initialize rectangle annotation using [AreaAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/areaannotation) class.
*   Adjust the position, size and color of the rectangle.
*   Set other properties like **page number, background, opacity, style, pen width**, **messages**, and **time**.
*   Add the created rectangle annotation to the Annotator.
*   Save the annotated PDF to the path using the [Save](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.



{{< figure align=center src="images/rectangle-area-annotation.jpg" alt="Add Rectangle or Area Annotation Programmatically">}}


The following code sample shows how to add rectangle/area annotation to a PDF document using C#.

<code>

## Add Oval or Ellipse Annotation to PDF using C# {#block-6792f088-c842-4df2-90a3-2bd26ac36b13}

The following are the steps to add oval annotation or ellipse annotation to a PDF document in C#.



{{< figure align=center src="images/ellipses-annotation.jpg" alt="Add Ellipses or Oval Annotation Programatically">}}


*   Load the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   Initialize ellipse annotation using [EllipseAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/ellipseannotation) class.
*   Set the position and size of the initialized ellipse annotation.
*   Add the created ellipse annotation to the Annotator object.
*   Provide the path and save the annotated PDF using the [Save](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

The following code sample shows how to add oval or ellipse annotation to a PDF document using C#.

<code>

## Insert Distance Annotation to PDF using C# {#block-f06d6a98-ca85-4719-b6a2-b365d0035939}

Similarly, you can add the distance annotation to mark the distance between two points. The following are the steps to add distance annotation to the PDF document.



{{< figure align=center src="images/distance-annotation.jpg" alt="Add Distance Annotation Programmatically">}}


*   After loading the PDF document, initialize distance annotation using [DistanceAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/distanceannotation) class.
*   Set the appearance of the annotation.
*   Add the distance annotation to the Annotator object.
*   Specify the path and save the annotated PDF at the given location.

The following code sample shows how to add distance annotation to a PDF document using C#.

<code>

## Complete Code {#block-10d3da51-836d-484c-9306-c11381d251ee}

To sum up, here is the complete code with the output showing all the added **annotations** and **messages** with **replies**.



{{< figure align=center src="images/added-annotations-to-pdf.jpg" alt="Added Annotations to PDF">}}


The following C# code below adds, arrow, rectangle, ellipse, distance annotations, messages, and replies to a PDF file.

<code>

## Remove Annotations from PDF in C# {#block-91763ab5-7e32-4dce-9139-9cad856edcc4}

The following are the steps to remove all the annotations from a PDF file.

*   Load the PDF document.
*   Initialize saving options using [SaveOptions](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.options/saveoptions) class.
*   Set the annotation types to None.
*   Save the PDF file. It will have no annotation in it.

The following code shows how to remove annotations from a PDF file using C#.

<code>

## Conclusion {#block-2248d63a-2641-40e6-898a-41c7aa86ec91}

In short, you have learned how to add annotations to PDF within .NET applications using C#. Specifically we added arrow, ellipse, area, and distance annotations to PDF file. Further, you have also seen how to remove all the annotations from any PDF file. Now, you can think to build your own document annotator .NET application.

To learn more about GroupDocs.Annotation for .NET, you can visit the [documentation](https://docs.groupdocs.com/annotation/net/) and the [GitHub](https://github.com/groupdocs-annotation) repository. For further queries, contact the support on the [forum](https://forum.groupdocs.com/).

## See Also {#block-80fdbca1-b18d-4773-a492-68f1dfa393b3}

*   [Add Watermark to Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)
*   [Annotate PDF files in Java](https://blog.groupdocs.com/2021/04/18/annotate-pdf-files-using-java/)



