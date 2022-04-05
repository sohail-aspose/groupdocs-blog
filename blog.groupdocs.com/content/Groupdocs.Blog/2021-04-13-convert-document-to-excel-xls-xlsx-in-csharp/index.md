---
title: 'Convert Documents to Excel XLS, XLSX in C#'
date: Tue, 13 Apr 2021 23:17:00 +0000
draft: false
url: /2021/04/13/convert-document-to-excel-xls-xlsx-in-csharp/
author: 'Shoaib Khan'
summary: 'If you have tabular data in PDF or Word documents format, you definitely need to convert it to Excel spreadsheets. This scenario becomes complex when there are many spreadsheets or multiple workbooks. You surely need to automate this procedure. In this article, we will see how to convert PDF to Excel and also how to convert Word documents to Excel spreadsheet programmatically in C# using .NET API.

The following are the topics discussed briefly in this article:

*   .NET API – Convert documents to spreadsheets
*   Convert PDF to Excel
*   Convert Word to Excel
*   PDF or Word to Spreadsheet conversion with more options

[Continue Reading ...](https://blog.groupdocs.com/2021/04/13/convert-document-to-excel-xls-xlsx-in-csharp/)'
tags: ['convert PDF to Excel in csharp', 'Convert Word to Excel in CSharp', 'document conversion', 'PDF to Excel in C#', 'Word to Excel in C#']
categories: ['GroupDocs.Conversion Product Family']
---

If you have tabular data in PDF or Word documents format, you definitely need to convert it to Excel spreadsheets. This scenario becomes complex when there are many spreadsheets or multiple workbooks. You surely need to automate this procedure. In this article, we will see how to convert PDF to Excel and also how to convert Word documents to Excel spreadsheets programmatically in C# using .NET API.



{{< figure align=center src="images/pdf-word-to-xls-in-csharp.jpg" alt="Convert Word and PDF to Excel in C#">}}


The following are the topics discussed briefly in this article:

*   .NET API – Convert documents to spreadsheets
*   Convert PDF to Excel
*   Convert Word to Excel
*   PDF or Word to Spreadsheet conversion with more options

## .NET API - Convert to Spreadsheet formats

In this article, I will be using [GroupDocs.Conversion for .NET](https://products.groupdocs.com/conversion/net) to convert PDF and Word documents to spreadsheets using C#. It is the feature-rich API that allows document and image conversions in many file formats. To highlight some formats, the API supports word-processing documents, spreadsheets, presentations, AutoCAD drawings, eBooks, PDF, email files, Web pages, images, photoshop files, and many other document formats.

Download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/conversion/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert PDF to Excel in C#

The following are the step to convert a PDF document to an Excel spreadsheet.

*   Load the PDF file using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Initialize convert option using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/spreadsheetconvertoptions) class.
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method of Converter class with option.

The following code sample shows how to convert a PDF file to Excel XLSX format using C#.

{{< gist GroupDocsGists c119873f115a451030df2d9c9196f619 "ConvertPdfToExcel.cs" >}}

## Convert Word to Excel in C#

You can convert any word document to an Excel spreadsheet in the same manner as we converted the PDF file above. We just have to provide the right source file to convert into XLS or XLSX.

The following are the step to convert a Word document with DOC DOCX format to an Excel spreadsheet.

*   Load the Word file using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Initialize convert option using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/spreadsheetconvertoptions) class.
*   Call the [Convert](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method of Converter class with option.

The following code sample shows how to convert a DOC or DOCX file to Excel XLSX format using C#.

{{< gist GroupDocsGists c119873f115a451030df2d9c9196f619 "ConvertWordToExcel.cs" >}}

## PDF or Word to Spreadsheet Conversion with more options using C#

You can convert only some of the selected pages of your document. The API gives you the privilege to convert your document with different options that include:

*   Starting **Page Number**.
*   **Page Count** to convert.
*   **Specific Pages** for conversion.
*   **Format** to convert into.
*   **Password** for make the file protected.
*   **Zoom** to make it large or smaller.
*   **Watermark** on the converter file.

The following are the steps for how to convert some of the pages of a PDF file into XLSX format with different zoom using C#.

{{< gist GroupDocsGists c119873f115a451030df2d9c9196f619 "ConvertPdfToExcelAdv.cs" >}}

Here are the PDF file and the converted spreadsheet as output using the above code. It converted the second page of the PDF file into XLSX format.



{{< figure align=center src="images/pdf-to-xls-in-csharp.jpg" alt="Convert PDF to Excel XLS XLSX Programmatically">}}


## Get a Free API License {#Get-a-Free-API-License}

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without evaluation limitations.

## Conclusion

In this article, you have learned how to convert PDF and Word documents in an Excel spreadsheet using C#. Furthermore, you have also seen how we can convert any part of the document with options like zoom, watermark, and making it password-protected. You can now start building your own .NET bases document conversion application or integrate the feature(s) in your existing application.

For more details, options, and examples, you can visit the [documentation](https://docs.groupdocs.com/conversion/net) and the [GitHub](https://github.com/groupdocs-conversion) repository. For further queries, contact the support on the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert CAD Drawings to PDF in C#](https://blog.groupdocs.com/2020/11/08/convert-cad-drawings-to-pdf-in-csharp/)
*   [Convert Presentations to PDF in C#](https://blog.groupdocs.com/2020/03/05/convert-presentations-pptx-ppt-to-pdf-in-csharp/)
*   [Convert Excel Spreadsheets to PDF using C#](https://blog.groupdocs.com/2021/11/14/convert-excel-spreadsheets-to-pdf-using-csharp/)




