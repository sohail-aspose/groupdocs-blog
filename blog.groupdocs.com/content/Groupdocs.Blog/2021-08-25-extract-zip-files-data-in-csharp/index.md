---
title: 'Extract ZIP Files Data in C#'
date: Wed, 25 Aug 2021 12:43:51 +0000
draft: false
url: /2021/08/25/extract-zip-files-data-in-csharp/
author: 'Shoaib Khan'
summary: 'Archives like **ZIP, RAR, TAR, GZIP, BZIP2** are commonly used to store more than one file and folder in a single container. Another main reason for archive files is to reduce the total file size using compression algorithms. Just like parsing and extracting data from documents of various file formats, you can treat the archive files in the same way. You can extract the text, images, and even metadata from the files that are compressed within the archives. In this article, we will discuss **how to extract the ZIP archives data using C#** with your .NET applications.

The following topics are covered in this article:

*   .NET API for ZIP files data extraction
*   How to extract ZIP files data'
tags: ['Extract Archives in CSharp', 'Extract from ZIP in C#', 'unzip data in C#']
categories: ['GroupDocs.Parser Product Family']
---

Archives like **ZIP, RAR, TAR, GZIP, BZIP2** are commonly used to store more than one file and folder in a single container. Another main reason for archive files is to reduce the total file size using compression algorithms. Just like parsing and extracting data from documents of various file formats, you can treat the archive files in the same way. You can extract the text, images, and even metadata from the files that are compressed within the archives. In this article, we will discuss **how to extract the ZIP archives data using C#** with your .NET applications.

The following topics are covered below:

*   [.NET API for ZIP files data extraction](#dotnet-zip-files-extraction-api)
*   [How to extract ZIP files data](#how-to-extract-zip-data)

## .NET API to Extract ZIP files Data {#dotnet-zip-files-extraction-api}

[GroupDocs.Parser](https://products.groupdocs.com/parser/) provides the document parsing solution for developers. I will be using its [.NET API to extract ZIP files data](https://products.groupdocs.com/parser/net/) within the C# examples of this article. The API further allows extraction of text, images, and metadata from a long list of [supported document formats](https://docs.groupdocs.com/parser/net/supported-document-formats/) like word-processing documents, presentations, spreadsheets, emails, databases, eBooks, and many others.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/parser) or install the API by adding its package to your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.parser).

```
PM> Install-Package GroupDocs.Parser
```

## How to Extract ZIP Files Data in C# {#how-to-extract-zip-data}

The [GroupDocs.Parser for .NET](https://products.groupdocs.com/parser/net/) supports data extraction from various compression file formats like ZIP, RAR, TAR, BZIP2, & GZIP. After retrieving the collection of files from the compressed file, you can further extract any kind of data from each file.

The following steps show how to extract ZIP files data and retrieve text from each enclosed file in C#.

*   Load the ZIP archive using **[Parser](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser)** class.
*   Obtain the attachments using **_[GetContainer](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser/methods/getcontainer)_** method
*   Traverse the collection of attachments.
*   For each attachment, you can get its different kind of data using respective methods of the **Parser** class.

The source code shows how to extract the ZIP files data using C#. In this example, I will be extracting the whole text from all the files within the ZIP archive.

{{< gist GroupDocsGists 184c6265993d61b5f7a8f106835337dc "ExtractDataFromZipArchive.cs" >}}

The output of the above source code shows the text retrieved from one of the PDF files within the ZIP file.

```
 -----------------------------------
 Name: sample.pdf
 File Size: 33370 Bytes
 -----------------------------------

 Heading

 This is the first paragraph of the sample document that contains some sample
 text, bulleted list, numbered list and more.

    •  Bullet Item 1
    •  Bullet Item 2
    •  Bullet Item 3
 
 This is the second paragraph of the sample document and after this, there is a
 numbered list: 

    1. Numbered Item 1
    2. Numbered Item 2
    3. Numbered Item 3 
```

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, you learned how to extract ZIP archives data using C# within your .NET application. More specifically you can now extract data from ZIP, RAR, TAR, GZIP, and BZIP files. You can even build your own data extraction .NET application for compressed files. For more details or learning about the API, visit the [documentation](https://docs.groupdocs.com/parser/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Extract Images from Documents using C#](https://blog.groupdocs.com/2020/10/28/extract-images-from-pdf-word-excel-ppt-using-csharp/)
*   [Extract Images from EPUB, FB2, CHM eBooks in C#](https://blog.groupdocs.com/2021/02/26/extract-images-from-ebooks-in-csharp/)
*   [Read PDF Form Fields using C#](https://blog.groupdocs.com/2020/12/23/parse-and-extract-data-from-pdf-forms-in-csharp/)




