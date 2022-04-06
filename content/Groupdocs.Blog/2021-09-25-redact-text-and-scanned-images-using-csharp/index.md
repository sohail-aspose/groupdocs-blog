---
title: 'Redact PDF Scanned Documents in C#'
date: Sat, 25 Sep 2021 09:31:01 +0000
draft: false
url: /2021/09/25/redact-text-and-scanned-images-using-csharp/
author: 'Shoaib Khan'
summary: 'We often need to hide the confidential and sensitive information within the documents. In other articles, we have discussed the different strategies to search words and even search synonyms within multiple documents. This article guides you about **how to redact PDF text and text in images within a document using C#**.'
tags: ['Blackout Text', 'Blackout Text in PDF', 'redact documents', 'Redact in CSharp', 'redact pdf', 'Redact PDF in CSharp', 'Redact Text in CSharp', 'Redact Text in Image', 'Redact Text in PDF']
categories: ['GroupDocs.Redaction Product Family']
---

We often need to hide the confidential and sensitive information within the documents. In other articles, we have discussed the [different strategies to search words](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in-documents-using-csharp/) and even [search synonyms within multiple documents](https://blog.groupdocs.com/2021/09/14/find-synonyms-of-words-using-csharp/). This article guides you about **how to redact PDF text and text in images within a document using C#**.

The following topics will be covered below:

*   [Text and image redaction - .NET API](#redaction-dotnet-api)
*   [Redact PDF text and scanned Information using C#](#redact-text-and-scanned-text)

## .NET API for Text and Image Redaction {#redaction-dotnet-api}

[GroupDocs.Redaction](https://products.groupdocs.com/redaction/) provides the [document redaction .NET API](https://products.groupdocs.com/redaction/net/) that allows hiding and removing confidential information within documents of various file formats. Along with the simple text redaction and rasterization, the API also allows identifying the text in images that may have been inside any document like most commonly used scanned PDF files. The complete list of [supported file formats](https://docs.groupdocs.com/redaction/net/supported-document-formats/) is available in the documentation.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/redaction) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.redaction).

### Install via Package Manager Console```
PM> Install-Package GroupDocs.Redaction
```

### Install via NuGet Package Manager



{{< figure align=center src="images/GroupDocs.Redaction-NuGet-Package-Install-1024x802.jpg" alt="GroupDocs.Redaction - NuGet Package - Install">}}


## Redact PDF Text and Scanned Image Text using C# {#redact-text-and-scanned-text}

There are many different [ways to find and replace text in documents](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in-documents-using-csharp/) that have already been discussed. You can find specific words in any document, find with case sensitivity, or by using regular expressions. I will be using the following PDF document, that contains some text and also an image with some text in it. Here we will combine the OCR and redaction process using GroupDocs.Redaction for .NET. Firstly, we will identify the text in the document and also the text which is inside the image of the document. Secondly, we will cover it with a black box to demonstrate how to programmatically hide any legal or confidential information even if is as text within a scanned document image.



{{< figure align=center src="images/PDF-with-text-and-scanned-image.jpg" alt="PDF with text and scanned image">}}


The following steps will detect and replace the text in a PDF document, that contains regular text along with some text within an embedded image.

*   Prepare the redactor settings using any OCR Connector.
*   Load the PDF document using [Redactor](https://apireference.groupdocs.com/redaction/net/groupdocs.redaction/redactor) class with the prepared settings and any specific loading options.
*   Define the [replacement option](https://apireference.groupdocs.com/redaction/net/groupdocs.redaction.redactions/replacementoptions). I have defined to black out the text.
*   For the text redaction, use the appropriate text selection strategy. I have used [RegEx](https://apireference.groupdocs.com/redaction/net/groupdocs.redaction.redactions/regexredaction).
*   Apply the redactions using the [Apply](https://apireference.groupdocs.com/redaction/net/groupdocs.redaction/redactor/methods/apply/index) method.
*   Save the redacted document using [Save](https://apireference.groupdocs.com/redaction/net/groupdocs.redaction/redactor/methods/save/index) method.

The following source code redacts the selected text within a PDF document using C#.

{{< gist GroupDocsGists f7e22d6719c21108d804756913b2ca3f "RedactTextInImage.cs" >}}

The output of the above code is as follows that black out the selected text of the PDF document.



{{< figure align=center src="images/Redacted-PDF-with-text-and-scanned-image.jpg" alt="Redact PDF text and scanned image text">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To sum up, you have learned to redact text in documents. More importantly and precisely, we discussed how to redact text in images within a PDF document using C#. We selected the text to redact using regular expressions, however, it can be selected using many different ways as discussed earlier. Later we blackout the search results using a black rectangle box over the searched text.

For more details to learn about the API, visit the [documentation](https://docs.groupdocs.com/redaction). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Find and Replace Words in Documents using C#](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in-documents-using-csharp/)
*   [Find and Remove Watermarks from Documents in C#](https://blog.groupdocs.com/2020/11/27/find-and-remove-watermarks-from-documents-in-csharp/)
*   [Add or Remove Annotations within Word files using C#](https://blog.groupdocs.com/2021/06/23/annotate-word-documents-using-csharp/)




