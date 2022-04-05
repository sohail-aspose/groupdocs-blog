---
title: 'Text Indexing and Search your Directories using C#'
date: Fri, 29 May 2020 07:30:00 +0000
draft: false
url: /2020/05/29/search-text-by-indexing-in-csharp-net/
author: 'Shoaib Khan'
summary: ''
tags: ['search in chunk', 'search text in csharp', 'search text in folders in csharp', 'search text in parts', 'text searching using csharp']
categories: ['GroupDocs.Search Product Family']
---

Using the .NET API, you can perform searching by parts and specify the number of search threads in C#. This feature will be more beneficial when you search text in large indexes that contain thousands of documents. Furthermore, you can now get the start & end time, and the total search time to get the search results.

The Following codf snippet shows how to create an index and then search text in chunks from the mentioned folder in C# using [GroupDocs.Search for .NET](https://products.groupdocs.com/search/net). To utilize the best performance, and updated features, I would recommend you [install](https://www.nuget.org/packages/GroupDocs.Search/) and use the latest version of API.

## Search Text by Indexing in C#

The following example shows how to perform the search by parts/chunks.

*   Create the [Index](https://apireference.groupdocs.com/net/search/groupdocs.search/index) with your index folder.
*   [Add](https://apireference.groupdocs.com/search/net/groupdocs.search/index/methods/add) your documents folder in the created index.
*   Set the [Search Option](https://apireference.groupdocs.com/search/net/groupdocs.search.options/searchoptions) and set your [IsChunkSearch](https://apireference.groupdocs.com/search/net/groupdocs.search.options/searchoptions/properties/ischunksearch) to true for search by chunk/parts
*   Call the [Search](https://apireference.groupdocs.com/net/search/groupdocs.search/index/methods/search/index) method of your index by providing your search query and searching options.
*   Now in the result, you may traverse each segment using [Search Next](https://apireference.groupdocs.com/search/net/groupdocs.search/index/methods/searchnext) and passing it [Chunk Search Token](https://apireference.groupdocs.com/search/net/groupdocs.search.results/searchresult/properties/nextchunksearchtoken) as a parameter.

```
string indexFolder = @"c:\\MyIndex\\";
string documentsFolder = @"c:\\MyDocuments\\";
string query = "Einstein";
// Creating an index in the specified folder
Index index = new Index(indexFolder);
// Indexing documents from the specified folder
index.Add(documentsFolder);
// Creating a search options instance
SearchOptions options = new SearchOptions();
options.IsChunkSearch = true; // Enabling the search by chunks
// Starting the search by chunks
SearchResult result = index.Search(query, options);
Console.WriteLine("Document count: " + result.DocumentCount);
Console.WriteLine("Occurrence count: " + result.OccurrenceCount);
// Continuing the search by chunks
while (result.NextChunkSearchToken != null)
{
    result = index.SearchNext(result.NextChunkSearchToken);
    Console.WriteLine("Document count: " + result.DocumentCount);
    Console.WriteLine("Occurrence count: " + result.OccurrenceCount);
}
```

For any suggestions, confusion, or queries related to the [.NET Search API](https://products.groupdocs.com/search/net), you may use the [forum](https://forum.groupdocs.com/c/search) for a quick response. You may quickly create a thread to share your thoughts.

## See Also

*   [Find and Replace Text in PDF using C#](https://blog.groupdocs.com/2022/02/19/find-and-replace-text-in-pdf-using-csharp/)
*   [Find and Replace Words in Word Documents using C#](https://blog.groupdocs.com/2022/02/15/find-and-replace-text-in-word-using-csharp/)




