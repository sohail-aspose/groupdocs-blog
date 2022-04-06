---
title: 'Strikethrough Text in Documents using C#'
date: Sat, 18 Dec 2021 19:10:44 +0000
draft: false
url: /2021/12/18/strikethrough-text-in-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'There are cases where you need to point out the content that has mistakes or it is no more valid. Crossed out is one of the ways to mark the invalid content within the documents. In order to automate the striking out within .NET applications, this article shows **how to strikethrough text in documents using C#**.'
tags: ['Cross out Text', 'Cross out Text in CSharp', 'Strikeout Text', 'Strikethrough Text', 'Strikethrough Text in CSharp']
categories: ['GroupDocs.Annotation Product Family']
---



{{< figure align=center src="images/strikethrough-text-using-csharp.jpg" alt="StrikeThrough Text using C#">}}


There are cases where you need to point out the content that has mistakes or it is no more valid. Crossing out is one of the ways to mark the invalid content within the documents. So, in order to automate the striking out within .NET applications, this article shows **how to strikethrough text in documents using C#**.

The following topics are discussed in this article.

*   [.NET API for Strikethrough Annotations](#strikethrough-text-dotnet-api)
*   [How to Strikeout Text in Documents](#strikethrough-text-using-csharp)

## .NET API to Strikethrough Text {#strikethrough-text-dotnet-api}

[GroupDocs.Annotation](https://products.groupdocs.com/annotation/) is a document and image annotation solution that allows automating various annotation types within multiple document formats. Therefore, I will use its .NET API in the examples of this article to strikethrough text within the documents. In addition to the strikeout annotation, there are many other [supported annotation types](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels) mentioned in the [documentation](https://docs.groupdocs.com/annotation/net/).

Download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/annotation/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.comparison).

```
PM> Install-Package GroupDocs.Annotation
```

## How to Strikethrough Text in Documents using C# {#strikethrough-text-using-csharp}

Let's quickly start to strike out the identified mistakes with the document. The following steps allow you to strikethrough the text in documents using C#.

*   Load the source document using [Annotator](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator) class.
*   Create and define the strikethrough annotation using [StrikeoutAnnotation](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation.models.annotationmodels/strikeoutannotation) class.
    *   Set the strikeout line color.
    *   Opacity, document page number
    *   Coordinates and other properties
*   Add the prepared strikeout annotation to the annotator using [Add()](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/add/index) method.
*   Save the annotated document using the [Save()](https://apireference.groupdocs.com/annotation/net/groupdocs.annotation/annotator/methods/save/index) method.

The following C# code example crosses out the selected text in a PDF document.

{{< gist GroupDocsGists 685b95eda9e5db503efb2b123574c5af "StrikethroughText.cs" >}}

## Get a Free API License

You can use GroupDocs.Annotation for .NET for free by [getting a temporary license](https://purchase.groupdocs.com/temporary-license).

## Conclusion

To sum up, you learned to add strikethrough annotation using C#. Using this annotation, you can programmatically strike out the text within Word, PDF, spreadsheet, presentation documents. Similarly, you can try various other annotation types according to your requirement.

Learn more about **GroupDocs.Annotation for .NET** by visiting its [documentation](https://docs.groupdocs.com/annotation/net). You can build your own annotator application for the [supported document formats](https://docs.groupdocs.com/annotation/net/supported-document-formats/). You can contact us for queries via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Highlight PDF using Annotations in C#](https://blog.groupdocs.com/2021/10/12/highlight-pdf-with-annotations-using-csharp/)
*   [Wavy Underline in Documents using C#](https://blog.groupdocs.com/2021/12/04/add-wavy-underline-in-documents-using-csharp/)




