---
title: 'Merge PDF, Word Documents, Spreadsheets, Presentation Files in C#'
date: Wed, 19 Aug 2020 18:20:42 +0000
draft: false
url: /2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/
author: 'Shoaib Khan'
summary: ''
tags: ['Merge Documents in CSharp', 'Merge Excel Sheets in CSharp', 'Merge PDF Files in CSharp', 'Merge PPT PPTX in CSharp', 'Merge Word Docs in CSharp']
categories: ['GroupDocs.Merger Product Family']
---

Today, we will learn to programmatically merge PDF, Word documents, spreadsheets, presentations using C#. In an earlier post, we have seen the [merging and splitting of documents using Java](https://blog.groupdocs.com/2020/05/20/merge-pdf-word-excel-powerpoint-documents-in-java/).



{{< figure align=center src="images/merge-documents-with-csharp-dotnet.png" alt="merge multiples pdf, word, excel, ppt files using csharp dotnet">}}


This article will also show you the code examples regarding:

*   [Merge PDF files](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/#merge-pdf-in-csharp)
*   [Merge Word documents](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/#merge-word-files-in-csharp)
*   [Merge selective pages](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/#merge-pages-in-csharp)
*   [Merge spreadsheets and presentations](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/#merge-documents-in-csharp)

I will be using the [GroupDocs.Merger for .NET](https://products.groupdocs.com/merger/net) in all the examples below. Before you proceed, you may get the API from either of the following options:

*   Install the package from [NuGet](https://www.nuget.org/packages/GroupDocs.Merger/) Packages Gallery.
*   [Download](https://downloads.groupdocs.com/merger/net) the MSI or DLLs from the downloads section of GroupDocs.

## Merge PDF Files in C# {#merge-pdf-in-csharp}

Following simple 3 lines of code combines 2 PDF files into 1 PDF document.

*   Start with the first document using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Call the [Join](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/join/index) method of Merger class and pass the second document to merge.
*   Call [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method to save the combined document.

```
// Merge 2 PDF files in C#
using (Merger merger = new Merger(@"document1.pdf"))
{
    merger.Join(@"document2.pdf");
    merger.Save(@"merged.pdf");
}
```

[Join](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/join/index) method has several overloaded methods that allow to merge documents or selective pages of different documents via file path, using a stream, or a remote URL.

## Merge Multiple Word Documents in C# {#merge-word-files-in-csharp}

The similar above code allows combining two or more files of MS Word and OpenDocument formats without losing the format. Just to give an idea, you can merge .doc, .docx, .docm, .dot, .dotx, .dotm, .rtf, .odt, .ott etc. Below is the 3 liner code that merges two MS Word DOCX files.

```
// Merge Word files in C#
using (Merger merger = new Merger(@"c:\\document1.docx"))
{
    merger.Join(@"c:\\document2.docx");
    merger.Save(@"c:\\merged.docx");
}
```

## Merge Pages of Multiple files - C# {#merge-pages-in-csharp}

Not only the whole document but we can also merge selective pages from multiple documents to get a combined single document.

```
// Merge selective pages
string filePath = @"c:\\sample.docx";
string filePath2 = @"c:\\sample2.docx";
string filePathOut = @"c:\\output\\result.docx";

JoinOptions joinOptions = new JoinOptions(1, 4, RangeMode.OddPages);

using (Merger merger = new Merger(filePath, loadOptions))
{
    merger.Join(filePath2, joinOptions);
    merger.Save(filePathOut);
}
```

## Merge Spreadsheets, Presentations and other Documents in C# {#merge-documents-in-csharp}

Along with the documents like PDF and Word, we can merge the presentations, spreadsheets, and many other formats with no different way. Just change the file name and type accordingly in the above code, you will get your merged document.

```
using (Merger merger = new Merger(@"filepath1.xxx"))
{
    merger.Join(@"filepath2.xxx");
    merger.Save(@"xyz.xxx");
}
```

## Check File Format Support First

Your requirement may be of a bit different file type, so it is better to know first that either the required document is supported for merge by the API or not. The following code gets all the file types supported by the Merger API.

```
foreach (FileType fileType in FileType
        .GetSupportedFileTypes()
        .OrderBy(fileType => fileType.Extension))
{
    Console.WriteLine(fileType);
}
```

Here is the output of the above code that displays file formats.

```
Bitmap Image File (.bmp)
Comma Separated Values File (.csv)
Excel Binary Spreadsheet (.xlsb)
Excel Macro-Enabled Add-In (.xlam)
Excel Open XML Macro-Enabled Spreadsheet (.xlsm)
Excel Open XML Macro-Enabled Spreadsheet Template (.xltm)
Excel Open XML Spreadsheet (.xlsx)
Excel Open XML Spreadsheet Template (.xltx)
Excel Spreadsheet (.xls)
Excel Template File (.xlt)
Hypertext Markup Language File (.html)
JPEG Image (.jpeg)
LaTeX Source Document (.tex)
MHTML Web Archive (.mht)
MIME HTML File (.mhtml)
OneNote Document (.one)
Open eBook File (.epub)
OpenDocument Document Template (.ott)
OpenDocument Presentation (.odp)
OpenDocument Presentation Template (.otp)
OpenDocument Spreadsheet (.ods)
OpenDocument Text Document (.odt)
Plain Text File (.txt)
Portable Document Format File (.pdf)
Portable Network Graphic (.png)
PostScript File (.ps)
PowerPoint Open XML Presentation (.pptx)
PowerPoint Open XML Slide Show (.ppsx)
PowerPoint Presentation (.ppt)
PowerPoint Slide Show (.pps)
Rich Text Format File (.rtf)
Tab Separated Values File (.tsv)
Visio Drawing (.vsdx)
Visio Drawing Template (.vstx)
Visio Drawing XML File (.vdx)
Visio Macro-Enabled Drawing (.vsdm)
Visio Macro-Enabled Drawing Template (.vstm)
Visio Macro-Enabled Stencil File (.vssm)
Visio Stencil File (.vssx)
Visio Stencil XML File (.vsx)
Visio Template XML File (.vtx)
Word Document (.doc)
Word Document Template (.dot)
Word Open XML Document (.docx)
Word Open XML Document Template (.dotx)
Word Open XML Macro-Enabled Document (.docm)
Word Open XML Macro-Enabled Document Template (.dotm)
XML Paper Specification File (.xps)
```

## Know more about the .NET Merger API

In case you want to know more about the .NET Merger API of GroupDocs, please visit the [documentation](https://docs.groupdocs.com/merger/net/getting-started/) or contact us on the [forum](https://forum.groupdocs.com/c/merger) about any query.

Thanks.




