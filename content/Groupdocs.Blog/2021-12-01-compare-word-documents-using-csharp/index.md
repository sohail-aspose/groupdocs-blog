---
title: 'Compare Word Documents using C#'
date: Wed, 01 Dec 2021 09:58:00 +0000
draft: false
url: /2021/12/01/compare-word-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'Word processing documents are the most common way to draft contracts, agreements, papers, and many other official documents. If you need to compare and merge two Word documents, just like the track changes option of Microsoft Word, we can programmatically do it within our .NET applications. In this article, we will discuss **how to compare two Word documents and highlight the identified differences using C#**. Additionally, we will look at how to compare password-protected documents, **accept and reject changes**, and compare more than two documents with C# examples.'
tags: ['automate document comparison', 'compare two word documents', 'compare two word documents and highlight differences', 'Compare Word Documents CSharp', 'compare word files in c#', 'GroupDocs Comparison', ]
categories: ['GroupDocs.Comparison Product Family']
---

Word processing documents are the most common way to draft contracts, agreements, papers, and many other official documents. If you need to compare and merge two Word documents, just like the track changes option of Microsoft Word, we can programmatically do it within our .NET applications. In this article, we will discuss **how to compare two Word documents and highlight the identified differences using C#**. Additionally, we will look at how to compare password-protected documents, **accept and reject changes**, and compare more than two documents with C# examples.



{{< figure align=center src="images/compare-word-files-using-csharp.jpg" alt="Compare Word Documents to find differences using .NET API">}}


The following topics are discussed here:

*   [Document Comparison .NET API](#doc-comparison-dotnet-api)
*   [Compare Two Word Documents](#compare-two-word-files)
*   [Accept or Reject Identified Changes in Word Document](#accept-reject-changes)
*   [Compare More than Two Word Documents](#compare-multiple-word-documents)
*   [Compare Password Protected Word Files](#compare-password-protected-word-docs)

## .NET API to Compare Word Documents {#doc-comparison-dotnet-api}

[GroupDocs.Comparison](https://products.groupdocs.com/comparison/) provides a .NET API that allows [comparing and then merging various documents of multiple file-formats](https://docs.groupdocs.com/comparison/net/supported-document-formats/) within the .NET application. I will use its .NET API i.e. [GroupDocs.Comparison for .NET](https://products.groupdocs.com/comparison/net/) to compare Word documents.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/comparison/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.comparison).

```
PM> Install-Package GroupDocs.Comparison
```

## Compare Word Documents using C# {#compare-two-word-files}

If you have two versions of a document, you can compare the documents to find their differences (additions, deletions) and create a new document that shows all the changes. The following are the steps to compare any two Word documents and highlight the differences.

*   Load the first Word document using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add the second file to **Comparer** using [Add()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/add/index) method.
*   Compare the get changes summary by just calling [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method.

The following C# code shows how to compare Word documents and get the changes in the resultant document.

{{< gist GroupDocsGists 2bc5a8376473a179e59310fd3dc23a9f "CompareWordDocs.cs" >}}

## Accept or Reject Identified Changes of Word Documents using C# {#accept-reject-changes}

Similar to the track changes option of MS Word, you can accept or reject each identified change. The following are the steps to compare and then accept or reject the identified changes within the Word documents.

*   Load the source document and add target Word document(s) using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Make the comparison of loaded documents using [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method.
*   Get the identified changes using [GetChanges()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/getchanges/index) method.
*   Now you can traverse the changes and set [ComparisonAction](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison.result/comparisonaction) of each change.
    *   For each change you can select **Accept**, or **Reject**.
*   When done with changes, call the [ApplyChanges()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/applychanges/index) method to get the resultant document having the applied changes.

The following C# source code compares two Word documents and then accepts an identified change and then rejects another one.

{{< gist GroupDocsGists 2bc5a8376473a179e59310fd3dc23a9f "AcceptRejectComparedChanges.cs" >}}

## Compare More than Two Documents using C# {#compare-multiple-word-documents}

Similarly, more than two documents can be compared in one go. The following are the steps to compare multiple Word documents for differences and highlight the identified changes.

*   Load the first Word document using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Keep adding the other document(s) to **Comparer** using the [Add()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/add/index) method.
*   Call the [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method to get the changes & summary of changes.

The following C# code shows how to compare more than two Word documents and get the changes in the resultant document.

{{< gist GroupDocsGists 2bc5a8376473a179e59310fd3dc23a9f "CompareMultipleDocs.cs" >}}

## Compare Password Protected Word Documents using C# {#compare-password-protected-word-docs}

If your documents are password-protected, just provide their password while loading the documents. The following steps show how we can compare the content of password-protected documents using C#.

*   Prepare the loading options for source and target documents by providing the password.
*   Load the source document using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add the target document to **Comparer** using the prepared loading options.
*   Get the differences summary by calling the [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method.

The following C# code example compares two password-protected Word files and generates the resultant document that highlights the differences.

{{< gist GroupDocsGists 2bc5a8376473a179e59310fd3dc23a9f "CompareProtectedWordDocs.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To conclude, we learned to compare two or more Word documents using C#. Further, after highlighting the differences, we learned to programmatically accept and reject the identified changes. In the end, we also discussed how could we compare the password-protected Word documents within .NET applications.

There are many other [customizations to control the comparison results](https://docs.groupdocs.com/comparison/net/comparison/), like setting the comparison sensitivity, showing only the summary page, ignoring **gaps**, and much more. Learn more about **GroupDocs.Comparison for .NET**. Visit its [documentation](https://docs.groupdocs.com/comparison/net) to start building your own document comparison applications for various [supported document formats](https://docs.groupdocs.com/comparison/net/supported-document-formats/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Compare Image using C# to Spot the Differences](https://blog.groupdocs.com/2021/01/06/compare-images-in-csharp-dotnet/)
*   [Compare PDF Documents using C# – Highlight, Accept or Reject Changes](https://blog.groupdocs.com/2021/12/10/compare-pdf-documents-using-csharp/)
*   [How to Compare Text, Word, and PDF Files in Java](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/)




