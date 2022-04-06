---
title: 'Extract Images from EPUB, FB2, CHM eBooks in C#'
date: Fri, 26 Feb 2021 07:26:57 +0000
draft: false
url: /2021/02/26/extract-images-from-ebooks-in-csharp/
author: 'Shoaib Khan'
summary: 'An electronic book, popularly known as **eBook**, is a book in digital form that is readable on various electronic devices. These devices include dedicated eReaders like Kindle, or laptops, desktop computers, and smartphones. There are many popular file formats of eBooks in-use in the market that include; **EPUB**, FictionBook **FB2**, Microsoft Compiled HTML Help - **CHM**, **DjVu**, **MOBI**, **PDF**, and many others. As a programmer, this article will help you to **programmatically extract images from eBooks in C#** within .NET applications.'
tags: ['Extract Images from CHM in CSharp', 'Extract Images from eBooks in CSharp', 'Extract Images from EPUB in CSharp', 'Extract Images from FB2 in CSharp', 'Parse eBooks in CSharp', 'Parse eBooks to Extract Images in CSharp']
categories: ['GroupDocs.Parser Product Family']
---

An electronic book, popularly known as **eBook**, is a book in digital form that is readable on various electronic devices. These devices include dedicated eReaders like [Kindle](https://en.wikipedia.org/wiki/Amazon_Kindle), or laptops, desktop computers, and smartphones. There are many popular file formats of eBooks in-use in the market that include; **EPUB**, FictionBook **FB2**, Microsoft Compiled HTML Help - **CHM**, **DjVu**, **MOBI**, **PDF**, and many others. As a programmer, this article will help you to **programmatically extract images from eBooks in C#** within .NET applications.

The following topics will be covered below:

*   [.NET API for Image Extraction from eBooks](#image-extraction-dotnet-api-for-ebooks)
*   [Extract Images from EPUB eBook in C#](#extract-images-from-epub-in-csharp)
*   [Extract Images from FB2, CHM eBooks in C#](#extract-images-from-fb2-chm-in-csharp)

## .NET API for Image Extraction from eBooks {#image-extraction-dotnet-api-for-ebooks}

For the extraction of images from eBooks, I will be using [GroupDocs.Parser for .NET](https://products.groupdocs.com/parser/net) API in the C# examples of this article. Along with the eBooks, this API supports parsing, and extraction of images from word-processing documents, spreadsheets, PDF, presentations, emails, ZIP archives, and many other document formats.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/parser/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.parser).

```
PM> Install-Package GroupDocs.Parser
```

## Extract Images from EPUB eBook in C# {#extract-images-from-epub-in-csharp}

Let's start with the EPUB eBook to parse it for images. Following steps followed by the C# code parses the EPUB eBook and extracts all the images in it.

*   Create [Parser](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser) class object.
*   Use [GetImages](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser/methods/getimages/index) method to extract all the images of the EPUB eBook.
*   Traverse the extracted images to [save](https://apireference.groupdocs.com/parser/net/groupdocs.parser.data/pageimagearea/methods/save/index) these, one by one.



{{< figure align=center src="images/alice.png" alt="alice EPUB" caption="EPUB eBook from the Adobe [Sample eBook Library](https://www.adobe.com/solutions/ebook/digital-editions/sample-ebook-library.html)">}}


The following C# code implements the mentioned parsing steps to parse to the above shown EPUB eBook and saves the extract images one by one to the disk.

{{< gist GroupDocsGists 4e52c001c3674a13067aadfc1c5e8016 "ExtractImagesFromEBooks.cs" >}}



{{< figure align=center src="images/alice-image-from-epub.jpg" alt="Extract Image from EPUB in C#">}}


As a result, all the available images will be saved. Here is one of the images shown as a sample.

You can save the extracted images in any of the following supported image file formats:

*   JPG
*   PNG
*   WEBP
*   GIF
*   BMP

## Extract Images from FB2, CHM eBooks in C# {#extract-images-from-fb2-chm-in-csharp}

If you have the eBook in FB2, CHM, or with some other format, you can extract its images in the same way. You just have to pass your eBook to the **Parser** constructor while creating the object. Then the **GetImages** method will be extracting images from any of the provided eBooks using the same C# code.

```
// Pass the FB2, CHM, PDF, or any other eBook to Parser contructor
Parser parser = new Parser("ebook.fb2"); // FB2
// Parser parser = new Parser("ebook.chm"); // CHM
// Parser parser = new Parser("ebook.pdf"); // PDF
IEnumerable<PageImageArea> images = parser.GetImages();
```

## Conclusion

I hope now you will be comfortable in programmatically getting all the images from eBooks with EPUB, FB2, CHM, and other file formats within your .NET applications. You can even build your own image extractor application using [GroupDocs.Parser for .NET](https://products.groupdocs.com/parser/net) API.

For more about the API, you may visit [documentation](https://docs.groupdocs.com/parser/net/) or open-source examples at GitHub. For any further issues, you can contact the quick support at the [forum](https://forum.groupdocs.com/c/parser/).

## See Also

*   [Extract Images from Word, Excel. PPT files using C#](https://blog.groupdocs.com/2020/10/28/extract-images-from-pdf-word-excel-ppt-using-csharp/)
*   [Extract Images from PDF Documents using C#](https://blog.groupdocs.com/2019/10/04/extract-images-from-pdf-files-in-csharp/)
*   [Extract Images from Documents using Java](https://blog.groupdocs.com/2020/10/27/extract-images-from-pdf-word-excel-ppt-using-java/)




