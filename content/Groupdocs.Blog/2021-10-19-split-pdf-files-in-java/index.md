---
title: 'Different Ways to Split PDF Files in Java'
date: Tue, 19 Oct 2021 14:41:58 +0000
draft: false
url: /2021/10/19/split-pdf-files-in-java/
author: 'Shoaib Khan'
summary: 'PDF is among the most famous file formats that support textual, graphical, and many other elements. One of the reasons for its popularity is its portability. In certain cases, you may need to split a large PDF file into multiple files. To address this programmatically, this article discusses different ways of **how to split PDF files in Java**.

The following topics are covered in this article:

*   Java API to Split PDF Files
*   Split PDF into Multi-Page Files
*   Split PDF into Multiple Single Pages Files
*   Extract Pages from PDF Files by Range in Java
*   Extract Pages from PDF Files using Even or Odd Filter in Java'
tags: ['PDF Separator', 'Separate PDF', 'Split API', 'Split PDF', 'Split PDF Files', 'Split PDF in Java']
categories: ['GroupDocs.Merger Product Family']
---



{{< figure align=center src="images/split-pdf-into-multiple-files-in-java.jpg" alt="Split PDF into Multiple Files in Java">}}


[PDF](https://docs.fileformat.com/pdf/) is among the most famous file formats that support textual, graphical, and many other elements. One of the reasons for its popularity is its portability. In certain cases, you may need to split a large PDF file into multiple files. To address this programmatically, this article discusses different ways of **how to split PDF files in Java**.

*   [Java API to Split PDF Files](#split-pdf-java-api)
*   [Split PDF into Multi-Page Files](#split-pdf-to-multipage)
*   [Split PDF into Multiple Single Pages Files](#split-to-single-pages)
*   [Extract Pages from PDF Files by Range in Java](#extract-pages-by-range)
*   [Extract Pages from PDF Files using Even or Odd Filter in Java](#extract-even-or-odd-pages)

## Java API to Split PDF Files {#split-pdf-java-api}

[GroupDocs.Merger](https://products.groupdocs.com/merger/) provides the solution to merge and split files of many different file formats. We will use its [Java API](https://products.groupdocs.com/merger/java/) to split PDF files in different ways. Download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/merger), or just use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-merger) configurations within your Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-merger</artifactId>
        <version>21.9</version> 
</dependency>
```

## Split PDF File into MultiPage Files in Java {#split-pdf-to-multipage}

The following steps guide how you can split a PDF file into multipage files:

*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Define the output file(s) format.
*   Define the page intervals using [SplitOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/SplitOptions).
*   Split the loaded PDF according to defined interval using [split()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#split(com.groupdocs.merger.domain.options.interfaces.ISplitOptions)) method.

The following code sample shows how to split PDF files into multipage files in Java.

{{< gist GroupDocsGists 0d92d118ccada913307231fbf3f741d2 "SplitPDFintoMultiPageFiles.java" >}}

## Split PDF File into Multiple Single-Page Files in Java {#split-to-single-pages}

The following steps guide how you can split a PDF to extract pages into multiple single-page files:

*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Define the output file(s) format.
*   Define the exact page numbers using [SplitOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/SplitOptions).
*   Split the loaded PDF according to defined pages using [split()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#split(com.groupdocs.merger.domain.options.interfaces.ISplitOptions)) method.

The following code sample shows how to split PDF files into multiple single-page files in Java.

{{< gist GroupDocsGists 0d92d118ccada913307231fbf3f741d2 "SplitPDFToSinglePages.java" >}}

## Extract Pages from PDF Files by Range in Java {#extract-pages-by-range}

The following steps guide how to extract pages from PDF by splitting according to the given range:

*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Define the output file(s) format.
*   Provide the pages range using [SplitOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/SplitOptions).
*   Use [split()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#split(com.groupdocs.merger.domain.options.interfaces.ISplitOptions)) method to split the loaded PDF according to the defined range.

The following code snippet shows how to split PDF and extract pages by providing range in Java.

{{< gist GroupDocsGists 0d92d118ccada913307231fbf3f741d2 "SplitPdfByRange.java" >}}

## Extract Pages from PDF Files using Even/Odd Filter in Java {#extract-even-or-odd-pages}

The following steps guide how to extract even/odd pages in the given range from PDF file by splitting:

*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Define the output file(s) format.
*   Provide the pages range using [SplitOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/SplitOptions).
*   Apply the even, odd, or all pages filter using [RangeMode](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/RangeMode).
*   Use [split()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#split(com.groupdocs.merger.domain.options.interfaces.ISplitOptions)) method to split the loaded PDF according to the defined filter.

The following code snippet shows how to extract all the odd/even pages in the defined range of a PDF file using Java.

{{< gist GroupDocsGists 0d92d118ccada913307231fbf3f741d2 "SplitPdfByRangeAndFilter.java" >}}

## Code Change Summary

The only thing that differs in the above scenarios is the way to create **SplitOptions**. You can use the following configurations as per your requirements within your code.

*   **For Multipage Files - Use Interval**: \[1,2\], \[3,4,5\], \[6,7\], \[8,9,10\].

```
new SplitOptions(outputFile,  new int[] { 3, 6, 8 }, SplitMode.Interval)
```

*   **Individual Pages**: \[3\], \[6\], \[8\]

```
new SplitOptions(outputFile, new int[] { 3, 6, 8 });
```

*   **To Extract Pages in Range**: \[3\], \[4\], \[5\]

```
new SplitOptions(outputFile, 3, 5);
```

*   **Range with Filter**: \[3\], \[5\], \[7\]

```
new SplitOptions(outputFile, 3, 7, (Integer)RangeMode.OddPages);
```

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, you have learned different ways to split PDF files in Java. First, we split the PDF file into multipage documents as well as in several single-page documents. Then one by one we extracted all the pages, and even/odd pages of the PDF file within the given range. Now you should be confident to build your own PDF splitter Java App using the GroupDocs.Merger API.

To learn more about the API, visit the [documentation](https://docs.groupdocs.com/merger). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Merge Multiple File Types into One using Java](https://blog.groupdocs.com/2021/06/13/merge-multiple-file-types-using-java/)
*   [Merge PDF, Word, Excel Documents in Java](https://blog.groupdocs.com/2020/05/20/merge-pdf-word-excel-powerpoint-documents-in-java/)
*   [Different Ways to Split PDF Files using C#](https://blog.groupdocs.com/2021/10/11/split-pdf-files-in-csharp/)




