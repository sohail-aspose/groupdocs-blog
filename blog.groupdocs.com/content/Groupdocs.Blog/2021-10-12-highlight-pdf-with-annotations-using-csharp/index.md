---
title: 'Highlight PDF using Annotations in C#'
date: Tue, 12 Oct 2021 14:08:00 +0000
draft: false
url: /2021/10/12/highlight-pdf-with-annotations-using-csharp/
author: 'Shoaib Khan'
summary: 'While reviewing or to attract viewer to an important content, you may need to highlight some part of the document. As a developer, you can automate this feature by using highlight annotations within your applications. In this article, you will learn **how to highlight text and any area in PDF files using C#**.

The following topics are covered in this article:

*   .NET API to Highlight in PDF
*   How to Programmatically Highlight in PDF'
tags: ['annotate PDF', 'Annotate PDF in CSharp', 'Highlight Annotation', 'Highlight PDF in CSharp', 'Highlight Text in PDF', 'Text Highlight']
categories: ['GroupDocs.Annotation Product Family']
---

While reviewing or to attract viewer to an important content, you may need to highlight some part of the document. As a developer, you can automate this feature by using highlight annotations within your applications. In this article, you will learn **how to highlight text and any area in PDF files using C#**.

The following topics are covered below:

*   [.NET API to Highlight in PDF](#highlight-pdf-dotnet-api)
*   [How to Programmatically Highlight in PDF](#how-to-highlight-pdf)



{{< figure align=center src="images/add-highlight-annotation-in-pdf-using-groupdocs.jpg" alt="Highlight Text in PDF - Programmatically">}}


## .NET API to Highlight in PDF {#highlight-pdf-dotnet-api}

[GroupDocs.Annotation](https://products.groupdocs.com/annotation/) provides .NET API that allows manipulating annotations and their automation in documents within .NET applications. I am using this API to highlight text in the PDF file in the example of this article.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/annotation) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.annotation).

```
PM> Install-Package GroupDocs.Annotation
```

## Highlight in PDF using C# {#how-to-highlight-pdf}

The following are the steps to highlight text or any area in PDF from your .NET application.

*   Load the source PDF document using [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   Create the [HighlightAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/highlightannotation) object.
*   Define the highlight properties like the color, opacity, page number, and points.
*   Add the defined highlighting to the loaded PDF document using [Add](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/add/index) method.
*   Save the annotated PDF using [Save](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

**Note:** You may change the highlight color, opacity, and other properties.

The following code sample shows how to highlight the text in PDF programmatically using C#.

{{< gist GroupDocsGists 489db43078dc098ec014662a64d3e81d "HighlightPDF.cs" >}}

The following is the output of the above code.



{{< figure align=center src="images/highlight-annotation-in-pdf-using-groupdocs.jpg" alt="Highlight Text in PDF - Programmatically">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, we have learned how to add highlight annotation in PDF files programmatically using C#. Additionally, we can change the highlight color, opacity, and other properties. Many [different types of annotations](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels) can be added in a similar way using the same API.

To learn about the API, visit the [documentation](https://docs.groupdocs.com/redaction). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Watermark PDF Files using C#](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/)
*   [Add Watermark to Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)
*   [Add or Remove Annotations or Markup Word files using C#](https://blog.groupdocs.com/2021/06/23/annotate-word-documents-using-csharp/)




