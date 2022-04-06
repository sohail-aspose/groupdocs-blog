---
title: 'Build Full-Text Search Solution in Java'
date: Sat, 07 Aug 2021 08:09:00 +0000
draft: false
url: /2021/08/07/build-full-text-search-solution-in-java/
author: 'Shoaib Khan'
summary: 'Full-text search is a way to search a text/query within a collection of documents. This approach quickly finds all instances of a term/phrase and it works by using text indexes. In this article, we will learn how to programmatically search full-text in documents using Java.'
tags: ['find in files and folder using Java', 'full text search', 'Full Text Search in Java', 'search via indexing']
categories: ['GroupDocs.Search Product Family']
---

Full-text search is a way to search a text/query within a collection of documents. This approach quickly finds all instances of a term/phrase and it works by using text indexes. In this article, we will learn how to programmatically search full-text in documents using Java.



{{< figure align=center src="images/TextSearch-1.png" alt="Full Text Search">}}


After this, you can implement various search techniques and build your search solution for word-processing documents, spreadsheets, presentations, HTML files, PDF files, eBooks, email messages, ZIP archives, and many other [document formats](https://docs.groupdocs.com/search/java/supported-document-formats/).

The following topics are covered below:

*   [Java API for Full-Text Search](#full-text-search-java-api)
*   [Full-Text Search](#full-text-search)
*   [Perform Search in Java](#perform-search)
*   [Highlight Search Results](#highlight-search-results)

## Java API for Full-Text Searching {#full-text-search-java-api}

[GroupDocs.Search](https://products.groupdocs.com/search/) provides a [full-text search Java API](https://products.groupdocs.com/search/java/) that can be integrated into any application without any third-party tool and software dependency. It allows you to [search over a large list of document formats](https://docs.groupdocs.com/search/java/supported-document-formats/). Some of the search techniques that can be performed using the API are as follows:

*   Case Sensitive Search
*   Regular Expression Search
*   Faceted Search
*   Fuzzy Search
*   Homophone Search
*   Synonym Search

### Download or Configure

You may download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/search), or just get the latest repository and dependency configurations for the pox.xml of your **maven-based** Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-search</artifactId>
        <version>21.3</version> 
</dependency>
```

## Full-Text Search using Java {#full-text-search}

There are two steps to perform the search within files stored in a folder.

*   Indexing
*   Perform Search

## Index files using Java

An index possesses scanned text of all the documents. Therefore, when you are going to perform a search operation, only the index is referenced, rather than the text of the original documents. To make it possible to search instantly across thousands of documents with the same or different file formats, you need to create an index and add these documents to it. When documents are indexed, the index is ready to handle the search queries.

The following simple two lines create an index and also add the documents folder to the index.

```
Index index = new Index("indexingFolderPath");
index.add("documentsFolderPath");
```

## Perform Search in Java {#perform-search}

After indexing multiple documents of the same or different formats like (Word, PDF, Excel, and HTML), we can move ahead to process a specific search query (search term “Draw”) over them. The following are the steps for how to perform text search on multiple documents within a folder using Java:

*   Specify the source folder of documents and index folder.
*   Create [Index](https://apireference.groupdocs.com/search/java/com.groupdocs.search/Index) using the index folder.
*   Add the source folder to the index.
*   Prepare the query string.
*   Perform a search using the [search](https://apireference.groupdocs.com/search/java/com.groupdocs.search/Index#search(com.groupdocs.search.SearchQuery)) method of Index class.
*   Traverse each search results for the properties of each document.

The following source code performs text search in Java on all the documents of the provided folder.

{{< gist GroupDocsGists 4fab169c40c4a8d27581d156002daea3 "SearchTextInDocs.java" >}}

We will get the document path and the number of occurrences of the search terms in all the documents with that specified folder. Here is the screenshot for visualization.



{{< figure align=center src="images/SearchTextOutput.jpg" alt="Full Search Text Output">}}


## Highlight Text Search Results in Java {#highlight-search-results}

Let’s now perform the same full-text search and also highlight all the occurrences that match your query.

The following steps show how to highlight the text search results:

*   Create [Index](https://apireference.groupdocs.com/search/java/com.groupdocs.search/Index)and add the documents folder to the index.
*   Prepare the query string.
*   Search the document folder using the [search](https://apireference.groupdocs.com/search/java/com.groupdocs.search/Index#search(com.groupdocs.search.SearchQuery)) method.
*   While traversing the results, create the highlighter using the [HtmlHighlighter](https://apireference.groupdocs.com/search/java/com.groupdocs.search.highlighters/HtmlHighlighter).
*   Use the highlight method to highlight the search results.

The following code generates the HTML output with highlighted search results using Java.

{{< gist GroupDocsGists 4fab169c40c4a8d27581d156002daea3 "HighlightSearchResults.java" >}}

As an output, we will get multiple HTML files. Each file will show the content of a separate document (e.g. excel.xlsx, source.docx, target.docx) with highlighted search terms/words. Given below is the highlighted HTML output of a DOCX file, TXT file, and PDF file obtained using the above code.



{{< figure align=center src="images/full-text-search-with-groupdocs.jpg" alt="Highlight full text search results in content using Java">}}


## Get a Free API License {#Get-a-Free-API-License}

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

In this article, we have learned to search text within multiple documents of a folder in Java. Further, we discussed how to programmatically highlight the text of search results in HTML format for MS Word files, TXT files, and PDF files using [GroupDocs.Search for Java](https://products.groupdocs.com/search/java/).

You may learn more about the API using [documentation](https://docs.groupdocs.com/search/). Many more examples are available at [GitHub](https://github.com/groupdocs-search). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Build your full-text search solution in C#](https://blog.groupdocs.com/2021/06/03/build-your-full-text-search-solution-in-csharp/)
*   [Word Search and Replace Text in PDF in Java](https://blog.groupdocs.com/2022/03/08/find-and-replace-text-in-pdf-in-java/)




