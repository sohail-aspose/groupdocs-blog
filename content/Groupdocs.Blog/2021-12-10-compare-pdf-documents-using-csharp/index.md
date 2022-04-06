---
title: 'Compare PDF Documents using C# - Highlight, Accept or Reject Changes'
date: Fri, 10 Dec 2021 10:20:37 +0000
draft: false
url: /2021/12/10/compare-pdf-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'Due to the fact that PDF is one of the most in-use formats of the digital world, it is often required to compare two versions of the same document. This article discusses, **how to compare two PDF documents and highlight the differences using C#**. Further, we will see how to compare password-protected PDF files, accept and reject changes, and also the comparison of more than two PDF files with C# examples.'
tags: ['compare PDF files', 'Compare PDF in CSharp', 'Compare PDF to Accept or Reject Changes in CSharp', 'pdf comparison']
categories: ['GroupDocs.Comparison Product Family']
---

Due to the fact that PDF is one of the most in-use formats of the digital world, it is often required to compare two versions of the same document. This article discusses, **how to compare two PDF documents and highlight the differences using C#**. Further, we will see how to compare password-protected PDF files, accept and reject changes, and also the comparison of more than two PDF files with C# examples.



{{< figure align=center src="images/compare-pdf-files-using-csharp.jpg" alt="Compare PDF Documents to find differences using .NET API">}}


The following topics are discussed here:

*   [PDF Comparison .NET API](#pdf-comparison-dotnet-api)
*   [Compare Two PDF Documents](#compare-two-pdf-files)
*   [Accept or Reject Identified Changes within PDF Documents](#accept-reject-changes)
*   [Compare More than Two PDF Documents](#compare-multiple-pdf-documents)
*   [Compare Password Protected PDF Files](#compare-password-protected-pdf-files)

## .NET API to Compare PDF Files {#pdf-comparison-dotnet-api}

[GroupDocs.Comparison for .NET](https://products.groupdocs.com/comparison/) is the API that allows comparison among multiple PDF documents and many other files of the same document format within the .NET applications. I will use this API in C# code examples of this article to compare PDF documents.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/comparison/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.comparison).

```
PM> Install-Package GroupDocs.Comparison
```

## Compare PDF Documents using C# {#compare-two-pdf-files}

If you have multiple copies of a PDF document, you can compare these files to find the differences (additions, deletions). After comparing the PDF content, you can create a new document that highlights all the identified changes. The following are the steps to compare two PDF documents and highlight the differences using C#.

*   Load the first PDF document using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add the second file to **Comparer** using [Add()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/add/index) method.
*   Compare both the PDF files and get the changes summary by calling [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method.

The following C# code snippet shows how to compare PDF documents and highlight the changes in the resultant document.

{{< gist GroupDocsGists bf49902dda69a05f94f88a324f67dd4e "ComparePDF.cs" >}}

## Accept or Reject Identified Changes of PDF Files using C# {#accept-reject-changes}

Just like the track changes features, you can programmatically accept or reject each identified change in PDF documents. The following steps show how to compare and then accept or reject the identified changes within the PDF documents.

*   Load the source and target PDF files using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Compare of loaded documents using [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method.
*   Get the identified changes using [GetChanges()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/getchanges/index) method.
*   Now traverse the changes and set the [ComparisonAction](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison.result/comparisonaction).
    *   Select **Accept**, or **Reject** for each change.
*   Call the [ApplyChanges()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/applychanges/index) method to get the resultant document with the accepted changes.

The following code snippet compares two PDF documents and then accepts an identified change and then rejects another one using C#.

{{< gist GroupDocsGists bf49902dda69a05f94f88a324f67dd4e "AcceptRejectPdfComparisonChanges.cs" >}}

## Compare More than Two PDF Files using C# {#compare-multiple-pdf-documents}

Similarly, you can compare more than two documents. The following are the steps that compare multiple PDF documents for differences and highlight the identified changes.

*   Load the first PDF files using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add other document(s) to **Comparer** using the [Add()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/add/index) method.
*   Compare all the PDF files using the [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method and get the changes & summary of changes.

The following example shows how to compare multiple PDF files in C# and get the changes in the resultant document.

{{< gist GroupDocsGists bf49902dda69a05f94f88a324f67dd4e "CompareMultiplePdfFiles.cs" >}}

## Compare Password Protected PDF Documents using C# {#compare-password-protected-pdf-files}

You can compare the password-protected files by just providing their passwords while loading these documents. The following steps show how we can compare the PDF content of password-protected documents using C#.

*   Prepare the loading options for source and target documents by providing the password.
*   Load the source document using [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add the target document to **Comparer** using the prepared loading options.
*   Get the differences summary by calling the [Compare()](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method.

The following example compares two password-protected PDF files and highlights the identified differences in a separate document using C#.

{{< gist GroupDocsGists bf49902dda69a05f94f88a324f67dd4e "CompareProtectedPdfFiles.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To conclude, we learned how to compare two or more PDF files using C#. Further, we highlighted the differences and programmatically accept or reject the identified changes. Lastly, we saw, how to compare password-protected PDF documents within .NET applications.

Several other [customizations](https://docs.groupdocs.com/comparison/net/comparison/) are available to control the comparison results. You can set the comparison sensitivity, show only the summary page, ignore **gaps**, etc. Learn more about **GroupDocs.Comparison for .NET** from the [documentation](https://docs.groupdocs.com/comparison/net). You can build your own document comparison applications for various [document formats](https://docs.groupdocs.com/comparison/net/supported-document-formats/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Image Comparison using C# & Spot the Differences](https://blog.groupdocs.com/2021/01/06/compare-images-in-csharp-dotnet/)
*   [Compare Word Documents using C#](https://blog.groupdocs.com/2021/12/01/compare-word-documents-using-csharp/)
*   [Compare Documents with Java Difference Library](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/)




