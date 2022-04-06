---
title: 'Convert Source Code to PDF in C#'
date: Fri, 03 Dec 2021 17:19:00 +0000
draft: false
url: /2021/12/03/convert-source-code-to-pdf-in-csharp/
author: 'Shoaib Khan'
summary: 'You sometimes need to convert the source code files to other formats. It may be for sharing or analysis purposes. This article discusses **how to convert Python**, PHP, Java, C#, C/C++** source code files to PDF** format within the .NET applications. Furthermore, we will programmatically password-protect the converted files.'
tags: ['Convert Source Code to PDF in CSharp', 'document rendering API', 'Java to PDF', 'PHP to PDF', 'Python Code to PDF', 'Source Code to PDF', 'source code viewer']
categories: ['GroupDocs.Viewer Product Family']
---



{{< figure align=center src="images/convert-source-code-to-pdf-in-csharp.jpg" alt="Convert Source Code to PDF using C#">}}


You sometimes need to convert the source code files to other formats. It may be for sharing or analysis purposes. This article discusses **how to convert Python**, PHP, Java, C#, C/C++** source code files to PDF** format within the .NET applications. Furthermore, we will programmatically password-protect the converted files.

*   [Source Code Conversion .NET API](#source-code-converter-dotnet-api)
*   [Java to PDF using C#](#java-to-pdf)
*   [Python to PDF using C#](#python-to-pdf)
*   [PHP to PDF - Protect the PDF file](#php-to-pdf)

## .NET API for Source Code Conversion {#source-code-converter-dotnet-api}

[GroupDocs.Viewer for .NET](https://products.groupdocs.com/viewer/net/) is the document viewer API and allows rendering the documents into PDF, HTML, and images with the .NET application. Today, we will use this API in examples to convert the source code files of different languages into PDF format.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/viewer/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.viewer).

```
PM> Install-Package GroupDocs.Viewer
```

## Convert Java Code to PDF using C# {#java-to-pdf}

No need to involve in complex configurations, just load the Java file, and transform it into PDF. The following steps guide you on how to convert the Java source code file to PDF using C#.

*   Load the Java file using the [Viewer](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer) class.
*   Set the output file and its options using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/pdfviewoptions) class.
*   Convert the file to PDF using the appropriate [View()](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer/methods/view) method.

The following C# example converts the complete Java source code file to PDF format.

{{< gist GroupDocsGists 1a4edc68b1c19980e1f5ff94cc2e4637 "JavaToPdf.cs" >}}

Here is the converted PDF of the Java file with highlighting using the above C# code. You can also add security to the converted PDF file. To learn about securing the files, jump below where the [PHP files are converted](#php-to-pdf).



{{< figure align=center src="images/java-to-pdf-programmatically.jpg" alt="Java source file converted to PDF using C#">}}


## Convert Python Code to PDF using C# {#python-to-pdf}

Why change the code if your source file format is changed? Let the API bear this pain. Just provide the .py file to the right method. The following steps show how to convert the Python code to PDF using C#.

*   Load the Python source file using the [Viewer](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer) class.
*   Define the output file path and configurations using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/pdfviewoptions) class.
*   Convert the .py file to PDF using the right [View()](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer/methods/view) method.

The following C# code example converts the Python source code file into PDF format.

{{< gist GroupDocsGists 1a4edc68b1c19980e1f5ff94cc2e4637 "PythonToPdf.cs" >}}

## Convert PHP to PDF using C# {#php-to-pdf}

Similarly, you can also convert the PHP files. Additionally, while converting your source code files, you can add security to the PDF files. Let's secure the code when it is converted. The following steps show the conversion of PHP files to PDF format with security in C#.

*   Load the PHP file using the [Viewer](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer) class.
*   Define the intended security of the PDF file using the [Security](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/security) class.
*   Set the passwords for opening and editing the resultant file.
*   Define the output file using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/pdfviewoptions) class.
*   Call the [View()](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer/methods/view) method to render the loaded PHP file into the protected PDF.

The following C# code snippet converts the PHP source code file into a password-protected PDF file.

{{< gist GroupDocsGists 1a4edc68b1c19980e1f5ff94cc2e4637 "PhpToPdfProtected.cs" >}}

Likewise, you can use this code for the source codes files of other [supported programming languages](https://docs.groupdocs.com/viewer/net/supported-document-formats/) like C#, C/C++, JS, Ruby, and more.

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To sum up, we learned to convert the source code files of various programming languages into PDF format using C#. The examples have shown the conversion of Java, Python, and PHP files to PDF format. Furthermore, we learned to secure the resultant PDF file. Using this API, you can start building your own source code viewer .NET application.

Learn more about **GroupDocs.Viewer** from the [documentation](https://docs.groupdocs.com/viewer) to build your own source code viewer application. For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Images to PDF Conversion in C#](https://blog.groupdocs.com/2021/05/19/convert-images-to-pdf-in-csharp/)
*   [Emails Files to PDF Conversion in C#](https://blog.groupdocs.com/2021/05/26/convert-eml-or-msg-file-to-pdf-in-csharp/)
*   [Excel Spreadsheets to PDF Conversion using C#](https://blog.groupdocs.com/2021/11/14/convert-excel-spreadsheets-to-pdf-using-csharp/)
*   [View Word Documents as HTML Responsive Page using C#](https://blog.groupdocs.com/2021/08/28/view-word-documents-as-html-responsive-page-using-csharp/)




