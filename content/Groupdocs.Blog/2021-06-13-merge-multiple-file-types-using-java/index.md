---
title: 'Merge Multiple File Types into One using Java'
date: Sun, 13 Jun 2021 05:49:00 +0000
draft: false
url: /2021/06/13/merge-multiple-file-types-using-java/
author: 'Shoaib Khan'
summary: 'Merging different documents is often required when you intend to gather the scattered data of different documents into one single file. In this article, you will learn to automate the documents merging process. This will show how to programmatically merge multiple documents of either the same or different file types into one file using Java. In another post, we discussed [merging multiple files of different formats using C#](https://blog.groupdocs.com/2021/05/04/merge-multiple-file-types-using-csharp/).

The following topics are covered in this article:

*   Java API - Merge Multiple Files
*   Merge PDF, Word, Excel files into one PDF
*   Merge Selective Pages of Multiple files into One File

[Continue Reading ...](https://blog.groupdocs.com/2021/06/13/merge-multiple-file-types-using-java/)'
tags: ['Merge Documents in Java', 'Merge Files in Java', 'Merge multiple file types in Java', 'Merge two or more file in Java']
categories: ['GroupDocs.Merger Product Family']
---

Merging different documents is often required when you intend to gather the scattered data of different documents into one single file. In this article, you will learn to automate the documents merging process. This will show how to programmatically merge multiple documents of either the same or different file types into one file using Java. In another post, we discussed [merging multiple files of different formats using C#](https://blog.groupdocs.com/2021/05/04/merge-multiple-file-types-using-csharp/).



{{< figure align=center src="images/merged-pdf-word-excel-files-to-pdf-in-java.jpg" alt="Merged PDF Word Excel Presentations to One PDF in Java">}}


The following topics are covered below:

*   [Java API - Merge Multiple Files](#java-api-to-merge-multiple-file-types)
*   [Merge PDF, Word, Excel files into one PDF](#merge-multiple-files-into-one-pdf-in-java)
*   [Merge Selective Pages of Multiple files into One File](#merge-selective-pages-of-multiple-files-into-one-pdf-in-java)

## Java API for Merging Multiple Document Types {#java-api-to-merge-multiple-file-types}

I will be using [GroupDocs.Merger for Java](https://products.groupdocs.com/merger/java/) to combine documents of different file formats into one file. The Java API allows joining various documents of the same or different formats into one file. Furthermore, it allows documents to split, trim, swap, move, remove, rotate, or arrange pages accordingly. Additionally, it supports passwords and their removal to manage the security of the [supported document formats](https://docs.groupdocs.com/merger/java/supported-document-formats/).

Some of the document types the API supports include; word-processing documents, spreadsheets, presentations, HTML, PDF, eBooks, Visio drawings, CSV, and TSV.

### Download and Configure

Get the document merger library from the downloads section. For Maven-based Java applications, add the following configuration within pom.xml. Afterward, you can try document merging java examples of this article as well as many more from [GitHub](https://github.com/groupdocs-merger). For the details, you may also visit the [API Reference](https://apireference.groupdocs.com/merger/java).

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-merger</artifactId>
        <version>21.3</version> 
</dependency>
```

## Merge PDF, Word, Excel files into one PDF in Java {#merge-multiple-files-into-one-pdf-in-java}

PDF documents can be combined with your Word documents, Excel spreadsheets, PowerPoint presentations, and other PDF documents with just a few lines of code. The following are the steps of how to merge documents of multiple file types into one file.

*   Load the initial document using the [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Combine the second document using the [join](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#join(java.io.InputStream)) method.
*   Keep merging the other documents (if required) using the same or similar **join** method.
*   Save the final combined document on path or stream using the relevant [save](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

The following source code shows how to merge PDF, Word, and Excel documents into one PDF file in Java.

{{< gist GroupDocsGists bcf021b81840177ce42499faf038e441 "MergeDifferentFiles.java" >}}

Similarly, documents with the same file types can be combined. The below-mentioned is the output obtained by joining a word document, a PDF document. and a spreadsheet using the above-mentioned Java code.



{{< figure align=center src="images/merged-pdf-word-excel-to-one-file.jpg" alt="Merge different file types into one PDF C#">}}


## Merge Selective Pages of Multiple PDF, Word, Excel files into One PDF in Java {#merge-selective-pages-of-multiple-files-into-one-pdf-in-java}



{{< figure align=center src="images/merged-selective-pages-of-pdf-word-excel-to-one-file.jpg" alt="Merge selective page of different file types into one PDF C#">}}


If you want to pick few pages from one document and some other selective pages from the next document, and so on. The API allows you to merge selective pages of multiple file types into one file in different ways.

*   Load the initial document using the [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Prepare the merging options with [JoinOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/JoinOptions) class.
*   Start merging the document using the [join](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#join(java.io.InputStream)) method.
*   Keep joining the documents by setting appropriate joining options for each document.
*   Save the final merged document using the [save](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

The following source code shows how to merge the first page of a Word document and the even sheets of Excel spreadsheet in the provided range in Java with a PDF document. The output will be a single PDF file.

{{< gist GroupDocsGists bcf021b81840177ce42499faf038e441 "MergeSelectivePages.java" >}}

## Get a Free API License {#Get-a-Free-API-License}

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you learned how to merge two or more documents of similar or different file types into one file using Java with your application. Additionally, you learned how to combine selective pages of multiple file types into one file.

You can learn more about GroupDocs.Merger using the [documentation](https://docs.groupdocs.com/merger). In case you have queries, contact us via [forum](https://forum.groupdocs.com/).

## See Also

*   [Split Files or Merge Documents in Java](https://blog.groupdocs.com/2020/05/20/merge-pdf-word-excel-powerpoint-documents-in-java/)
*   [Merge multiple files of different formats into one using C#](https://blog.groupdocs.com/2021/05/04/merge-multiple-file-types-using-csharp/)




