---
title: 'Find and Remove Watermarks from Documents in C#'
date: Fri, 27 Nov 2020 14:21:34 +0000
draft: false
url: /2020/11/27/find-and-remove-watermarks-from-documents-in-csharp/
author: 'Shoaib Khan'
summary: 'Today, we will have a look at **how to find and remove watermarks from documents in C#**. There can be text and image-based watermarks in a document. We can easily search and programmatically remove such watermarks from many PDF, Word, Excel, PowerPoint, and Visio supported documents.'
tags: ['find and remove watermarks in csharp', 'find watermarks in csharp', 'remove watermarks in csharp', 'Watermarking API for .NET']
categories: ['GroupDocs.Watermark Product Family']
---

Today, we will have a look at **how to find and remove watermarks from documents in C#**. There can be text and image-based watermarks in a document. We can easily search and programmatically remove such watermarks from many PDF, Word, Excel, PowerPoint, and Visio supported documents.

Following topics will be covered in this article:

*   [.NET API for removing watermarks](#watermark-removing-api-for-dotnet)
*   [Find watermarks in documents using C#](#find-watermarks-in-documents-using-csharp)
*   [Remove watermarks from documents in C#](#remove-watermarks-from-documents-in-csharp)



{{< figure align=center src="images/find-and-remove-watermarks-using-groupdocs.watermark-1.png" alt="Find and Remove Watermarks from Documents using GroupDocs API">}}


## .NET API for Watermark Removal {#watermark-removing-api-for-dotnet}



{{< figure align=center src="images/groupdocs-watermark-net.png" alt="Watermark API for .NET - GroupDocs">}}


[GroupDocs.Watermark for .NET](https://products.groupdocs.com/watermark/net) is a fast and efficient watermarking API that requires no additional software. It allows adding watermarks to documents and images in such a way that would be hard for third-party tools to remove. It also lets C# developers easily remove watermarks from many **Microsoft** and **OpenOffice** file formats of **word-processing documents**, **spreadsheets**, **presentations**, **Visio drawings**, and **PDF** documents in .NET applications. All the [supported file formats](https://docs.groupdocs.com/watermark/net/supported-document-formats/) are mentioned in the [documentation](https://docs.groupdocs.com/watermark/net/).

Now, I will be showing examples that will be finding and removing watermarks. So, it will be better if you prepare the environment beforehand by following any of the suitable options:

*   [NuGet](https://www.nuget.org/packages/groupdocs.watermark)
*   [Direct Download](https://downloads.groupdocs.com/watermark/net): MSI installer and DLLs
*   **Package Manager Console:**

```
PM> Install-Package GroupDocs.Watermark
```

## Find Watermarks in Documents using C# {#find-watermarks-in-documents-using-csharp}

[Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker), [PossibleWatermarkCollection](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.search/possiblewatermarkcollection) (the collection of [PossibleWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.search/possiblewatermark)) are the classes of the API to find various kinds of watermarks in documents with various search criteria and remove them quickly. Following are the steps for the basic search of all the watermarks in any provided document using C#. You can further refine your search for watermarks and this is shown later in this article.

*   Create the **Watermarker** class object with the source document file.
*   Call the **Search** method. It will return all the possible watermarks from the document.
*   Traverse the watermarks collection to display data or perform any action on each watermark.

{{< gist GroupDocsGists 000f76d654bdac72017a72ca8304a3f2 "SearchWatermarks.cs" >}}

## Remove Watermarks from Documents in C# {#remove-watermarks-from-documents-in-csharp}

From all the searched watermarks, we can remove any watermark or all the watermarks at once. The main thing here, whether you have successfully found the watermark(s) that you want to delete or not. What if there are lots of different types of watermarks in a document? The API gives various options to refine your search for watermarks. The following code removes the watermark from a PDF document by specifying the index of collection using C#.

{{< gist GroupDocsGists 4fa618502d15fc884614db7d7601ec53 "RemoveWatermark.cs" >}}

## More Search Criteria for Watermarks

There are many other ways to find watermarks with certain criteria. After the selective search, we can remove the watermark(s) from the collection by using **Remove**, **RemoveAt**, or **Clear** method accordingly. Here are some of the ways to find watermarks from the provided documents:

*   Find and remove watermarks with specific text
*   Search watermarks with RegEx (Regular Expression) and remove
*   Search watermark with specified text formatting
*   Find and remove hyperlink watermarks

### Find and Remove Watermarks with Specific Text

You can search for text watermarks by specifying the exact string using the following C# code:

```
 // Find possible watermarks containing the specified text
TextSearchCriteria textSearchCriterion = new TextSearchCriteria("© 2020");
PossibleWatermarkCollection possibleWatermarks = watermarker.Search(textSearchCriterion);
```

### Search for Watermarks with RegEx and Remove

If there is some pattern in the watermark's text, you can provide regular expression (RegEx) to search for these watermarks and can remove later accordingly using the following C# code. This code will fetch all the watermarks with ©YYYY.

```
// Search Watermarks by Regular Expression
Regex regex = new Regex(@"^© \\d{4}$");
TextSearchCriteria textSearchCriterion = new TextSearchCriteria(regex);
PossibleWatermarkCollection possibleWatermarks = watermarker.Search(textSearchCriterion);
```

### Find and Remove Watermarks with Specific Text Formatting

You can also find the watermarks having some specific text formatting like Font name, min/max font size, bold/italic/underlined, etc.

```
TextFormattingSearchCriteria criterion = new TextFormattingSearchCriteria()
{
    FontName = "Arial",
    MinFontSize = 19,
    MaxFontSize = 42,
    FontBold = true
};
PossibleWatermarkCollection watermarks = watermarker.Search(criterion);
watermarks.Clear();
```

### Find and Remove Hyperlink Watermarks

You can use the RegEx to find text watermarks having hyperlinks in the content. Later you can check in the collection if there are hyperlink watermarks in the search result. These can be removed by any of the removal methods. The following C# code removes all the watermarks with hyperlinks.

```
PossibleWatermarkCollection watermarks = watermarker.Search(new TextSearchCriteria(new Regex(@"anyurl\\.com")));
for (int i = watermarks.Count - 1; i >= 0; i--)
{
    // Is watermark the hyperlink?
    if (watermarks\[i\] is HyperlinkPossibleWatermark)
    {
        watermarks.RemoveAt(i);
    }
}
```

There are many other ways to refine your [search for watermarks](https://docs.groupdocs.com/watermark/net/searching-watermarks/). You can visit [documentation](https://docs.groupdocs.com/watermark/net/) for more detail. For queries, visit the [forum](https://forum.groupdocs.com/c/watermark).

## Conclusion

I believe that you will now be more confident in finding and removing text watermarks as well as image watermarks from Word documents, Excel spreadsheets, Powerpoint presentations, PDF documents, and Visio drawings using C# within your .NET applications.

## See Also

*   [Add Watermark to Images or Images in Documents using C#](https://blog.groupdocs.com/2019/10/21/add-watermark-to-images-using-csharp-dotnet-api/)
*   [Add Watermark to Images in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)
*   [Find and Remove Watermarks from Documents in Java](https://blog.groupdocs.com/2019/10/10/find-and-remove-watermarks-from-documents-in-java/)




