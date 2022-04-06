---
title: 'How to Split PDF Files using C#'
date: Mon, 11 Oct 2021 04:14:00 +0000
draft: false
url: /2021/10/11/split-pdf-files-in-csharp/
author: 'Shoaib Khan'
summary: '[PDF](https://docs.fileformat.com/pdf/) is one of the most commonly used file formats which is highly portable. As a developer, you may have faced the scenario to split large PDF files programmatically. Today, this article discusses different ways of **how to split PDF files using C# in .NET applications**.'
tags: ['PDF Separator', 'Separate PDF', 'Split API', 'Split PDF', 'Split PDF Files', 'Split PDF using C#']
categories: ['GroupDocs.Merger Product Family']
---



{{< figure align=center src="images/split-pdf-into-multiple-files-using-csharp.jpg" alt="Split PDF into Multiple Files using C#">}}


[PDF](https://docs.fileformat.com/pdf/) is one of the most commonly used file formats which is highly portable. As a developer, you may have faced the scenario to split large PDF files programmatically. In one of the articles, we learned to [split the PDF files in Java](https://blog.groupdocs.com/2021/10/19/split-pdf-files-in-java/). Today, this article discusses different ways of **how to split PDF files using C# in .NET applications**.

*   [.NET API to Split PDF Files](#split-pdf-dontet-api)
*   [Split PDF into Multi-Page Files](#split-pdf-to-multipage)
*   [Extract Pages from PDF Files by Range](#extract-pages-by-range)
*   [Extract Pages from PDF Files using Even or Odd Filter](#extract-even-or-odd-pages)
*   [Split PDF into Multiple Single Pages Files](https://blog.groupdocs.com/wp-admin/post.php?post=23730&action=edit#split-to-single-pages)

## .NET API to Split PDF Files {#split-pdf-dontet-api}

In order to split PDF files, we will use [GroupDocs.Merger for .NET](https://products.groupdocs.com/merger/net/). It is the API that allows rapid development to integrate features with very few lines of code. In addition to splitting, it supports [merging, swapping, or trimming documents of different file formats](https://docs.groupdocs.com/merger/net/supported-document-formats/).

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/merger) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.merger).

```
PM> Install-Package GroupDocs.Merger
```

## Split PDF File into MultiPage Files using C# {#split-pdf-to-multipage}

The following steps guide how you can split PDF files into multipage files using C#:

*   Define the output file(s) format.
*   Define the page intervals using [SplitOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/splitoptions).
*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Split the loaded PDF according to defined interval using [Split()](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/split/index) method.

The following code sample shows how to split PDF files into multipage files.

{{< gist GroupDocsGists 4a46dd994d515ad491f5bcdcf6ec11d6 "SplitPDFintoMultiPageFiles.cs" >}}

## Extract Pages from PDF Files by Range {#extract-pages-by-range}

The following steps guide how to extract pages from PDF using C# by splitting according to the given range:

*   Define the output file(s) format.
*   Provide the pages range using [SplitOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/splitoptions).
*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Use [Split()](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/split/index) method to split the loaded PDF according to the defined range.

The following code snippet shows how to split PDF and extract pages by providing the range.

{{< gist GroupDocsGists 4a46dd994d515ad491f5bcdcf6ec11d6 "SplitPdfByRange.cs" >}}

## Extract Even/Odd Pages from PDF Files using C# {#extract-even-or-odd-pages}

The following steps guide how to extract even/odd pages from a PDF file by splitting within the given range by just applying filters in C#:

*   Define the output file(s) format.
*   Provide the pages range using [SplitOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/splitoptions).
*   Apply the filter for even, odd, or all pages using [RangeMode](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/rangemode).
*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Use [Split()](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/split/index) method to separate the loaded PDF according to the defined filter.

The following code snippet shows how to extract all the odd/even pages in the defined range of a PDF file.

{{< gist GroupDocsGists 4a46dd994d515ad491f5bcdcf6ec11d6 "SplitPdfByRangeAndFilter.cs" >}}

## Split PDF File into Multiple Single-Page Files {#split-to-single-pages}

The following steps guide how we can split a PDF to extract pages as multiple single-page files in C#:

*   Define the output file(s) format.
*   Define the exact page numbers using [SplitOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/splitoptions).
*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Split the loaded PDF according to defined pages using [Split()](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/split/index) method.

The following code sample shows how to split PDF files into multiple single-page files.

{{< gist GroupDocsGists 4a46dd994d515ad491f5bcdcf6ec11d6 "SplitPDFToSinglePages.cs" >}}

## Code Change Summary

In all the scenarios, the thing that changes is the way to define **SplitOptions**. Here is the summary of the change in each code snippet for each scenario. You can use the following settings as per your requirements within your code. Here, I used a PDF file having 10 pages.

*   **For Multipage Files - Use Interval**: \[1,2\], \[3,4,5\], \[6,7\], \[8,9,10\].

```
new SplitOptions(outputFile,  new int[] { 3, 6, 8 }, SplitMode.Interval)
```

*   **Extract Pages in Range**: \[3\], \[4\], \[5\], \[6\]

```
new SplitOptions(outputFile, 3, 6);
```

*   **Range with Filter**: \[3\], \[5\], \[7\]

```
new SplitOptions(outputFile, 3, 8, (Integer)RangeMode.OddPages);
```

*   **Individual Pages**: \[3\], \[4\], \[9\]

```
new SplitOptions(outputFile, new int[] { 3, 4, 9 });
```

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, we discussed the ways to split PDF files using C#. First, we split the PDF file into multipage & single-page documents. We also extracted pages from PDF files. First, we extracted all the pages, and then even/odd pages within the given range. You can try building your own PDF splitting .NET App using GroupDocs.Merger API.

To learn more about the API, visit the [documentation](https://docs.groupdocs.com/merger). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Merge Documents using C#](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/)
*   [Merge Multiple File Types into Single Document using C#](https://blog.groupdocs.com/2021/05/04/merge-multiple-file-types-using-csharp/)
*   [Rearrange PDF Pages using C#](https://blog.groupdocs.com/2022/02/22/move-pdf-pages-using-csharp/)
*   [Rearrange Pages in Word using C#](https://blog.groupdocs.com/2022/02/05/move-word-pages-using-csharp/)
*   [How to Split PDF Files in Java](https://blog.groupdocs.com/2021/10/19/split-pdf-files-in-java/)




