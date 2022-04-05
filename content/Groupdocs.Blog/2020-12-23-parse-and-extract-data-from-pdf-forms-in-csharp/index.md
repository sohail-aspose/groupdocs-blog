---
title: 'Read PDF Form Fields using C#'
date: Wed, 23 Dec 2020 12:39:01 +0000
draft: false
url: /2020/12/23/parse-and-extract-data-from-pdf-forms-in-csharp/
author: 'Shoaib Khan'
summary: 'In this article, we will learn **how to read and parse PDF documents and then programmatically extract PDF form field values in C#**. Earlier, we have seen [how to extract values from PDF forms in Java](https://blog.groupdocs.com/2020/12/09/parse-and-extract-data-from-pdf-forms-in-java/). After reading these articles, if you have filled feedback forms, you can extract the values within your .NET & Java applications for analysis or save them in the database.



{{< figure align=center src="images/Extract-from-PDF-Form-in-csharp.jpeg" alt="Parse PDF Forms to Extract values in C#">}}


[Continue Reading](https://blog.groupdocs.com/2020/12/23/parse-and-extract-data-from-pdf-forms-in-csharp/)'
tags: ['Extract Text from PDF Forms in CSharp', 'Parse PDF Forms in CSharp', 'Read PDF Form Fields in CSharp']
categories: ['GroupDocs.Parser Product Family']
---

In this article, we will learn **how to read and parse PDF documents and then programmatically extract PDF form field values in C#**. Earlier, we have seen [how to extract values from PDF forms in Java](https://blog.groupdocs.com/2020/12/09/parse-and-extract-data-from-pdf-forms-in-java/). After reading these articles, if you have filled feedback forms, you can extract the values within your .NET & Java applications for analysis or save them in the database.



{{< figure align=center src="images/Extract-from-PDF-Form-in-csharp.jpeg" alt="Parse PDF Forms to Extract values in C#">}}


## .NET API to Parse and Extract Values from PDF Forms

[GroupDocs.Parser for .NET](https://products.groupdocs.com/parser/net) is an easy to use, and powerful parsing and data extraction API for the .NET applications. It supports text, metadata, and image extraction from word-processing and PDF documents, spreadsheets, presentations, emails, markups, ebooks, archives, and much more. One of the significant features and will also be shown below is the parsing of fillable PDF forms to extract the form field values using a small piece of C# code.

To test the below-mentioned and other examples of the API, you may download and install the API from [NuGet](https://www.nuget.org/packages/groupdocs.parser) or directly [download](https://downloads.groupdocs.com/parser/net) from GroupDocs downloads.

```
PM> Install-Package GroupDocs.Parser
```

## Extract Data from PDF Form Field using C#

The following simple steps tell how to parse PDF and then extract PDF form field values in C#.

*   Load the PDF file using [Parser](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser) class.
*   Parse the PDF form using [ParseForm](https://apireference.groupdocs.com/parser/net/groupdocs.parser/parser/methods/parseform) method.
*   Traverse the parsed collection to extract the form field values.

The following C# code example shows the extraction of field values of filled PDF forms within .NET applications.

{{< gist GroupDocsGists b64b2266ab7018b43e07dfa41aaa7cad "ParsePdfForms.cs" >}}

```
COMPANY: GroupDocs
EMAIL: everything@groupdocs.com
COUNTRY: Australia
```

## Conclusion

I am confident, that you will now feel comfortable in developing your own .NET based application that can parse PDF files and fetch values from fillable PDF form fields quickly and precisely. To add more features, you can learn more about the API from the [documentation](https://docs.groupdocs.com/parser/net/) articles and C# examples on [GitHub](https://github.com/groupdocs-parser/GroupDocs.Parser-for-.NET).

For queries and quick response, be in contact on the [forum](https://forum.groupdocs.com/c/parser).

## See Also

*   [Read PDF Form Fields using Java](https://blog.groupdocs.com/2020/12/09/parse-and-extract-data-from-pdf-forms-in-java/)
*   [Extract Images from Documents in C#](https://blog.groupdocs.com/2020/10/28/extract-images-from-pdf-word-excel-ppt-using-csharp/)




