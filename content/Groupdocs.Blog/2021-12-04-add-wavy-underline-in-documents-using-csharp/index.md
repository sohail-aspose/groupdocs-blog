---
title: 'Add Wavy Underline in Word, PDF &amp; Other Documents using C#'
date: Sat, 04 Dec 2021 15:37:01 +0000
draft: false
url: /2021/12/04/add-wavy-underline-in-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'Squiggly underlines are normally used to show inconsistencies in the document. We are quite familiar with these lines as Microsoft Word uses red squiggly underlines to indicate spelling mistakes and blue squiggly/wavy underlines for formatting issues. We can also add such underline annotations in documents programmatically. In this article, we will learn **how to add wavy underlines in Word, PDF, PPT, and other documents using C#**.'
tags: ['Annotation in CSharp', 'Squiggly Annotation in CSharp', 'Squiggly Underline in Word', 'Wavy Underline in CSharp', 'Wavy Underline in Word']
categories: ['GroupDocs.Annotation Product Family']
---

Squiggly underlines are normally used to show inconsistencies in the document. We are quite familiar with these lines as Microsoft Word uses red squiggly underlines to indicate spelling mistakes and blue squiggly/wavy underlines for formatting issues. We can also add such underline annotations in documents programmatically. In this article, we will learn **how to add wavy underlines in Word, PDF, PPT, and other documents using C#**.



{{< figure align=center src="images/adding-squiggly-annotation.jpg" alt="Add Squiggly Annotation to Documents">}}


The following topics are discussed below:

*   [.NET API for Wavy Underline / Squiggly Annotation](#wavy-underline-dotnet-api)
*   [Add Wavy Underline to Text in Word Documents - Squiggly Annotation](#wavy underline in word)
*   [Add Wavy Underline to Text in PDF, PPT, and other Documents](#wavy-underline-in-pdf-ppt-etc)

## .NET API for Wavy Underline - Squiggly Annotation {#wavy-underline-dotnet-api}

[GroupDocs.Annotation](https://products.groupdocs.com/annotation/) provides the annotation solution that allows manipulation and automation of various annotation types in documents within .NET applications. We will use its [GroupDocs.Annotation for .NET](https://products.groupdocs.com/annotation/net/) API to add a squiggly annotation in documents using C#.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/annotation) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.annotation).

```
PM> Install-Package GroupDocs.Annotation
```

## Add Wavy Underline to Text in Word (DOC/DOCX) using C# - Squiggly Annotation {#add-wavy-underline-in-word}

The following step shows how to insert a wavy underline in a Word document using C#.

*   **Load** the Word (DOC, DOCX) using the [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   **Create the wavy underline** using the [SquigglyAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/squigglyannotation) class.
*   **Personalize** the squiggly underline by setting its color, opacity, coordinates, page number, etc.
*   [**Add**](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/add/index) the squiggly annotation to the annotator.
*   **Save** the updated Word file using [Save()](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

The following C# code example adds the wavy underline to the selected text of the Word document.

{{< gist GroupDocsGists 0d25b0bfdc7cfaaa084bbaab8509adf9 "AddSquigglyAnnotationToWord.cs" >}}

You can add any other annotation type from various [AnnotationModels](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels).

## Add Wavy Underline to Text in PDF, PPT, and Other Documents using C# {#wavy-underline-in-pdf-ppt-etc}

Similarly, you can add the squiggly underline to any document using the same C# code (Check the documentation if your intended document file format is supported by the API).

The following are the steps for how to insert a wavy underline in a PDF document using C#.

*   **Load** the PDF document using the [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   **Create the squiggly underline** using the [SquigglyAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/squigglyannotation) class.
*   **Customize** the color, opacity, coordinates, page number, etc for the squiggly/wavy underline.
*   **Add** the squiggly annotation to the annotator using [Add()](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/add/index) method.
*   **Save** the updated PDF file using [Save()](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

The following C# code example adds the wavy underline to the selected text of the PDF file.

{{< gist GroupDocsGists 0d25b0bfdc7cfaaa084bbaab8509adf9 "AddSquigglyAnnotationToPDF.cs" >}}

## Conclusion

To sum up, we discussed how to add wavy/squiggly underline in Word documents using C#. Additionally, the same squiggly annotation can be added to other documents like PDF, PPT, and more. Squiggly annotation is a new addition to [many other annotation types offered by the API](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels).

Learn more about **GroupDocs.Annotation for .NET**. Visit its [documentation](https://docs.groupdocs.com/annotation/net) to start building your own document annotation applications for various [supported document formats](https://docs.groupdocs.com/annotation/net/supported-document-formats/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Add or Remove Annotations or Markup Word files using C#](https://blog.groupdocs.com/2021/06/23/annotate-word-documents-using-csharp/)
*   [Add or Remove Annotations from PDF files using Java](https://blog.groupdocs.com/2021/04/18/annotate-pdf-files-using-java/)




