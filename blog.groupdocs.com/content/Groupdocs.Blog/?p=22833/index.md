---
title: ''
date: 
draft: true
url: /?p=22833
author: 'Shoaib Khan'
summary: ''
tags: ['Uncategorized']
---



{{< figure align=center src="images/TextSearch-1.png" alt="Full Text Search">}}


Before we leap into the details, let's get an overview of this technique. Full-text search is basically a more advanced way to search a text/query over a collection of documents. This approach quickly finds all instances of a term and it works by using text indexes.

One of the examples of full-text search implementation is in Word processors and text editors. It helps you to find a phrase or word anywhere in the document.

## .NET API for Text Search

[GroupDocs.Search for .NET](https://products.groupdocs.com/search/net) is a full-text search, back-end API that can be integrated into any .NET application without any third-party tool or software dependency. It allows you to [search over a multitude of document formats](https://docs.groupdocs.com/search/net/supported-document-formats/) in your applications.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/search) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.search).

```
PM> Install-Package GroupDocs.Search
```

## Full-Text Search using C#

There are two main steps to perform or implement a full-text search.

*   Indexing
*   Perform Search

## Indexing

To make it possible to search instantly across thousands of documents with the same or different file formats, you need to create an index and add these documents to it.

### **What is an index?**

An index possesses scanned text of all the documents. Therefore, when you are going to perform a search operation (search a specific query), only the index is referenced, rather than the text of the original documents.

### **Index creation**

An index can be created in memory or on a disk. The index created in memory cannot be saved after exiting your program. In contrast, an index created on the disk may be loaded in the future to continue working. The following example shows how to create an index on a disk.

```
Index index = new Index("indexPath/FolderName/");
```

## Perform Text Search in C#

When documents are indexed, the index is ready to handle the search queries. The following are some of the search types that can be performed:

*   Case Sensitive Search
*   Regular Expression Search
*   Phrase Search
*   Faceted Search
*   Synonym Search
*   Wildcard Search

Starting with a use case. If we have multiple documents (Word, PDF, Excel, and HTML) and we want to perform a specific search query (search term "video") over them.

The following are the steps for how to perform text search on multiple documents within a folder:

*   Decide source documents folder and index folder.
*   Prepare the query string.
*   Create index using index folder.
*   Add the source documents folder to the index.
*   Perform a search using the Search method Index class.
*   Traverse and search results for each document's properties.

The following source code perform text search using C# on all the documents of the provided folder.

\[gist id="9600c1fffefa5e1d0edea71fb209d7a1" file="SearchTextInDocs.cs"\]

We will get the document path and the number of search term occurrences in all the documents available in the document folder. Here is the screenshot to visualize.



{{< figure align=center src="images/SearchTextOutput.jpg" alt="Full Search Text Output">}}


## Highlight Text Search Results in C#

Let's now perform the same text search, but this time we will highlight all the occurrences that match the query.

The following steps shows how to highlight the text search results:

*   Prepare the query string.
*   Create index using index folder path.
*   Add the source documents folder to the index.
*   Search the document folder using the Search method.
*   While traversing the search results, create the Highlighter.
*   Use the Highlight method of the Index class to highlight the search results.

The following code generates the HTML output with highlighted search results using C#.

\[gist id="9600c1fffefa5e1d0edea71fb209d7a1" file="HighlightSearchResults.cs"\]

As an output, we will get multiple HTML files. Each file will show the content of a different document (e.g. excel.xlsx, source.docx, target.docx) with highlighted search term/word. Given below is the highlighted HTML output of a DOCX file.



{{< figure align=center src="images/highlight-text-search-result.jpg" alt="Highlight full text search results in content">}}


## Get a Free API License {#Get-a-Free-API-License}

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

In this article, we have learned to search text within multiple documents of a folder using C#. Further, we discussed how to programmatically highlight the text of search results in HTML format.

You may learn more about GroupDocs.Search for .NET using [documentation](https://docs.groupdocs.com/search/). Many more examples are available at [GitHub](https://github.com/groupdocs-search). For queries, contact us via the [forum](https://forum.groupdocs.com/).



