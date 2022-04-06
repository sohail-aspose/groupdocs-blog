---
title: 'Merge Multiple File Types into Single Document using C#'
date: Tue, 04 May 2021 20:10:39 +0000
draft: false
url: /2021/05/04/merge-multiple-file-types-using-csharp/
author: 'Shoaib Khan'
summary: 'To combine the data that is present in multiple documents, and sometimes in documents of different file types, there comes the need to merge all your documents or the portion of the documents into one. In this article, you will learn, how to merge multiple documents of either the same or different file types in one file using C#.'
tags: ['Merge Documents in CSharp', 'Merge Files in CSharp', 'Merge multiple file types in CSharp', 'merge two or more files']
categories: ['GroupDocs.Merger Product Family']
---

To combine the data that is present in multiple documents, and sometimes in documents of different file types, there comes the need to merge all your documents or the portion of the documents into one. In this article, you will learn, how to programmatically merge multiple documents of either the same or different file types into one file using C#.



{{< figure align=center src="images/merged-pdf-word-excel-files-to-pdf-in-csharp.jpg" alt="Merged PDF Word Excel Presentations to One PDF in C#">}}


The following are the topics covered below:

*   [.NET API - Merge Multiple Document Types](#dotnet-api-to-merge-multiple-file-types)
*   [Merge PDF, Word, Excel files into one PDF](#merge-multiple-files-into-one-pdf-in-csharp)
*   [Merge Selective Pages of Multiple files into One File](#merge-selective-pages-of-multiple-files-into-one-pdf-in-csharp)

## .NET API for Merging Multiple Document Types {#dotnet-api-to-merge-multiple-file-types}

Today, I will be using GroupDocs.Merger for .NET to combine documents of different file formats into one file. The .NET API allows joining various documents of the same or different formats into one file. Furthermore, it allows documents to split, trim documents, and swap, move, remove, rotate, or arrange pages. Additionally, it supports setting or remove passwords to manage the security of the [supported document formats](https://docs.groupdocs.com/merger/net/supported-document-formats/).

Some of the document types the API supports include; word-processing documents, spreadsheets, presentations, HTML, PDF, eBooks, Visio drawings, CSV, and TSV.

Download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/merger/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.merger).

```
PM> Install-Package GroupDocs.Merger
```

## Merge PDF, Word, Excel files into one PDF in C# {#merge-multiple-files-into-one-pdf-in-csharp}

You can combine your PDF documents with your Word documents, presentations and Excel spreadsheets with just a few lines of code. The following are the steps of how to merge documents of multiple file types into one file.

*   Load the source document using the [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Keep merging other documents using the [Join](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/join/index) method.
*   Save the combined document as output using the [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

The following source code shows how to merge PDF, Word, and Excel documents into one PDF file in C#.

{{< gist GroupDocsGists a5fbd8bfba0cfddd998cd60a3089e584 "MergeDifferentFiles.cs" >}}

In the same way, you can also combine files of the same file format. The below-mentioned is the output obtained by joining a word document, a PDF document. and a spreadsheet using the above C# code.



{{< figure align=center src="images/merged-pdf-word-excel-to-one-file.jpg" alt="Merge different file types into one PDF C#">}}


## Merge Selective Pages of Multiple PDF, Word, Excel files into One PDF in C# {#merge-selective-pages-of-multiple-files-into-one-pdf-in-csharp}



{{< figure align=center src="images/merged-selective-pages-of-pdf-word-excel-to-one-file.jpg" alt="Merge selective page of different file types into one PDF C#">}}


Not always you want to combine the whole document. You may want to pick few pages from one document and some other pages from the next document, and so on. The API provides different ways to merge selective pages of multiple file types into one file.

*   Load the source document using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Set the merging options using [JoinOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/joinoptions) class.
*   Merge the document using the [Join](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/join/index) method.
*   Keep combining the documents by setting different joining options for each document.
*   Save the merged document using the [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

The following source code shows how to merge a PDF file with the first page of a Word document, and the even sheets of Excel workbook in the provided range, into a single PDF file using C#.

{{< gist GroupDocsGists a5fbd8bfba0cfddd998cd60a3089e584 "MergeSelectivePages.cs" >}}

## Conclusion

To sum up, you have seen how to merge two or more documents of different file types into one file using C# within .NET application. Additionally, you have learned how to combine just the selective pages of multiple file types.

You can learn more about GroupDocs.Merger for .NET using the [documentation](https://docs.groupdocs.com/merger/net). In case you would have queries, do let us know via our [forum](https://forum.groupdocs.com/).

## See Also

*   [Merge documents of the same format in C#](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/)
*   [Split or merge documents in Java](https://blog.groupdocs.com/2020/05/20/merge-pdf-word-excel-powerpoint-documents-in-java/)




