---
title: "'在 Java 中的多个文件中查找同音字'"
date: Thu, 13 Jan 2022 06:28:19 +0000
draft: false
url: /zh/2022/01/13/find-homophones-in-multiple-files-using-java/
author: 'Shoaib Khan'
summary: '**Synonyms** are words with similar meaning, and **Homophones** sounds the same but are different in meanings or spellings. We learned to [find synonyms in multiple documents using Java](https://blog.groupdocs.com/2021/10/03/find-synonyms-in-multiple-files-using-java/). Today, in this article, we will see **how to search homophones within multiple documents using Java**.

本文涵盖以下主题：

* Java API - 同音字搜索
* 使用 Java 在文档中查找同音字
*玩同音搜索结果'
tags: ['Find Homophone in Java', 'Find Homophones', 'Find Homophones in Files', 'Homophones']
categories: ['GroupDocs.Search Product Family']
---

**同义词**是具有相似含义的词，**同音词**听起来相同，但含义或拼写不同。我们学会了[使用 Java 在多个文档中查找同义词](https://blog.groupdocs.com/2021/10/03/find-synonyms-in-multiple-files-using-java/)。今天，在本文中，我们将了解**如何使用 Java 在多个文档中搜索同音字**。



{{< figure align=center src="images/Search-Homophones-in-Files.jpg" alt="使用 GroupDocs 在文件中搜索同音字">}}


下面将介绍以下主题：

* [Java API - 同音字搜索](#homophone-search-java-api)
* [使用 Java 在文档中查找同音字](#homophone-in-different-files)
* [播放同音字搜索结果](#print-homophone-search)

## 用于搜索同音字的 Java API {#homophone-search-java-api}

[GroupDocs.Search](https://products.groupdocs.com/search/) 展示了 Java API ([GroupDocs.Search for Java](https://products.groupdocs.com/search/net/))，它允许在任何特定文件夹的多个文件中查找任何单词及其同音字。它可以搜索[各种不同格式]的内容（https://docs.groupdocs.com/search/net/supported-document-formats/）。除了查找同音字外，API 还支持许多其他搜索技术，包括：

*区分大小写的搜索
* 模糊搜索
* 短语搜索
* 正则表达式搜索
* 同义词搜索
* 外卡搜索

您可以从 [下载部分](https://downloads.groupdocs.com/search) 下载 **JAR** 文件或使用最新的存储库和依赖项 [Maven](https://repository.groupdocs.com/ Java 应用程序中的 webapp/#/artifacts/browse/tree/General/repo/com/groupdocs) 配置。

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-search</artifactId>
        <version>21.8</version> 
</dependency>
``````
PM> Install-Package GroupDocs.Search
```

## Find Homophones in Multiple Files in Java {#homophone-in-different-files}

The following steps guide how to search homophones in multiple files of a folder in Java.

*   Define the search word query, indexing folder, and the container folder of your files.
*   Create [Index](https://apireference.groupdocs.com/search/java/com.groupdocs.search/Index) with the defined index folder.
*   Add the document's folder to the index.
*   Define the [SearchOptions](https://apireference.groupdocs.com/search/java/com.groupdocs.search.options/SearchOptions) and enable the homophoneSearch using [setUseHomophoneSearch()](https://apireference.groupdocs.com/search/java/com.groupdocs.search.options/SearchOptions#setUseHomophoneSearch(boolean)).
*   Perform the homophones search using [search()](https://apireference.groupdocs.com/search/java/com.groupdocs.search/Index#search(com.groupdocs.search.SearchQuery,%20com.groupdocs.search.options.SearchOptions)) method.
*   Use the properties of the retrived [SearchResult](https://apireference.groupdocs.com/search/java/com.groupdocs.search.results/SearchResult) as needed.

The following Java source code finds all the homophones within files of the defined folder. Further, you can also [manage your homophone dictionary](https://docs.groupdocs.com/search/java/homophone-dictionary/).

{{< gist GroupDocsGists e150579822915caefa017952b0f19b3d "SearchHomophonesInFilesAndFolders.java" >}}

The output of the above code is as follows:

```
查询：**对**
文件：2
出现次数：17
```

## Printing Homophone Search Results in Java {#print-homophone-search}

You can use the homophones search results by following the steps after getting the homophones and their occurrences from each document.

*   Traverse the search results.
*   Get each [FoundDocument](https://apireference.groupdocs.com/search/java/com.groupdocs.search.results/FoundDocument) using the [getFoundDocument()](https://apireference.groupdocs.com/search/java/com.groupdocs.search.results/SearchResult#getFoundDocument(int)) method.
*   Use the properties of each FoundDocument as required.
*   Now, traverse the fields of FoundDocument by getting [FoundDocumentField](https://apireference.groupdocs.com/search/java/com.groupdocs.search.results/FoundDocumentField).
*   Later, from each FoundDocumentField, get all the terms and their occurrences within each document.

The following Java code example prints the homophone search results along with the number of occurrences of each searched term.

{{< gist GroupDocsGists e150579822915caefa017952b0f19b3d "PrintingHomophoneSearchResults.java" >}}

The following is the output of the above code example.

```
查询：**对**
文件：2
总出现次数：17

文件：C:/documents/sample.docx
出现次数：11
领域：内容
    出现次数：11
对 3
仪式 4
赖特 1
写 3
文件：C:/documents/sample.txt
出现次数：6
领域：内容
    出现次数：6
对 4
写 2
```

## Search Homophones and Printing Results using Java - Complete Code {#search-and-print-synonyms-code}

The following Java code combines the above steps. Initially, it finds the homophones as per query, and then prints all the occurrences of homophones from each document within the provided folder.

{{< gist GroupDocsGists e150579822915caefa017952b0f19b3d "SearchHomophonesAndPrintResults.java" >}}

## Conclusion

To conclude, you learned how to find the words and their homophones from multiple documents within a specified folder using Java. You can try developing your own Java application for searching homophones using **GroupDocs.Search for Java**.

Learn more [about the Java Search Automation API](https://docs.groupdocs.com/search/java/) from the documentation. To experience its features, you can have a look at the available examples on the [GitHub](https://github.com/groupdocs-search) repository. Reach us for any query via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Search Homophones in Multiple Files in C#](https://blog.groupdocs.com/2022/01/04/find-homophones-in-multiple-files-using-csharp/)
*   [Find Synonyms of Words using Java](https://blog.groupdocs.com/2021/09/30/find-synonyms-of-words-using-java/)
*   [Build your Full Text Search Solution in Java](https://blog.groupdocs.com/2021/08/07/build-full-text-search-solution-in-java/)
*   [Find and Replace Words in Documents using Java](https://blog.groupdocs.com/2021/09/01/find-and-replace-text-in-documents-using-java/)
*   [Find and Remove Watermarks from Documents in Java](https://blog.groupdocs.com/2020/11/30/find-and-remove-watermarks-from-documents-in-java/)





