---
title: 'Create Hyperlinks in PDF using Annotations in C#'
date: Sat, 16 Oct 2021 01:00:00 +0000
draft: false
url: /2021/10/16/create-hyperlinks-in-pdf-using-annotations-in-csharp/
author: 'Shoaib Khan'
summary: 'Hyperlinks are normally used to associate external data to any specified area of the document. We can transform any part of the documents to hyperlinks using the link annotations. As a programmer, you can add these link annotations to documents within your .NET applications. In this article, we are going to discuss that **how to create hyperlinks in PDF files using C#**.

The following topics are covered in this article:

*   .NET API to Add Hyperlinks in PDF files
*   How to Programmatically Create Hyperlinks in PDF'
tags: ['annotate PDF', 'Annotate PDF in CSharp', 'Create Hyperlink in PDF', 'Link Annotation', 'Link Annotation in CSharp', 'Link Annotation in PDF']
categories: ['GroupDocs.Annotation Product Family']
---

Hyperlinks are normally used to associate external data to any specified area of the document. We can transform any part of the documents to hyperlinks using the link annotations. As a programmer, you can add these link annotations to documents within your .NET applications. In this article, we are going to discuss that **how to create hyperlinks in PDF files using C#**.

The following topics are covered below:

*   .NET API to Add Hyperlinks in PDF files
*   How to Programmatically Create Hyperlinks in PDF

*   [.NET API to Add Hyperlinks in PDF files](#hyperlink-dotnet-api)
*   [How to Programmatically Create Hyperlinks in PDF](#how-to-create-hyperlink-annotations)



{{< figure align=center src="images/add-link-annotation-in-pdf-using-groupdocs.jpg" alt="Create Link in PDF - Programmatically">}}


## .NET API to Create Hyperlinks in PDF {#hyperlink-dotnet-api}

[GroupDocs.Annotation](https://products.groupdocs.com/annotation/) provides the annotation solution for different kinds of applications. Its .NET API allows manipulation and automation of various annotations in documents within your .NET applications. We will use its [GroupDocs.Annotation for .NET](https://products.groupdocs.com/annotation/net/) API to create hyperlink annotations in the PDF file using C#.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/annotation) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.annotation).

```
PM> Install-Package GroupDocs.Annotation
```

## Create Hyperlinks in PDF using C# {#how-to-create-hyperlink-annotations}

The following are the steps to create hyperlinks anywhere in the PDF file using C#.

*   Load the source PDF document using [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   Create the [Link Annotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/linkannotation) object.
*   Define the hyperlink properties like url, page number, points, etc.
*   Add the defined hyperlink to the loaded PDF document using [Add](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/add/index) method.
*   Save the annotated PDF using [Save](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

The following code sample shows how to convert any part of the PDF file into a hyperlink using C#.

{{< gist GroupDocsGists 489db43078dc098ec014662a64d3e81d "AddHyperlinkInPDF.cs" >}}

The following is the output of the above code.



{{< figure align=center src="images/link-annotation-in-pdf-using-groupdocs.jpg" alt="Create Link in PDF - Programmatically">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you have learned how the link annotations can be added to create hyperlinks in PDF files using C#. Likewise, using link annotations, you can convert any part of the document into hyperlinks. Many other [annotation types](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels) can also be added in a similar way using the same API. Learn further about the API by visiting the [documentation](https://docs.groupdocs.com/redaction). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Watermark PDF Files using C#](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/)
*   [Add Watermark to Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)
*   [Highlight PDF using Annotations in C#](https://blog.groupdocs.com/2021/10/12/highlight-pdf-with-annotations-using-csharp/)
*   [Add or Remove Annotations or Markup Word files using C#](https://blog.groupdocs.com/2021/06/23/annotate-word-documents-using-csharp/)




