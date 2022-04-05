---
title: 'Convert Excel Spreadsheets to PDF using C#'
date: Sun, 14 Nov 2021 17:48:00 +0000
draft: false
url: /2021/11/14/convert-excel-spreadsheets-to-pdf-using-csharp/
author: 'Shoaib Khan'
summary: 'Excel (XLS, XLSX) and PDF files are among those document formats that are widely used in almost every business. For such commonly used files there are many scenarios in which we need to convert one file into another format. In this article, we will learn different ways for how to convert Excel spreadsheets into PDF format using C# with .NET applications.

The following topics are covered in this article:

*   .NET API for Excel Files to PDF Conversion
*   Excel Sheets to PDF Conversion
*   Sequence of Excel Sheets to PDF Conversion
*   Specific List of Excel Sheets to PDF Conversion
*   Convert Selected Cell Range from Excel Sheet to PDF'
tags: ['Convert Excel in CSharp', 'Convert Excel to PDF', 'Convert Excel to PDF in CSharp', 'Convert to PDF in CSharp', 'Excel to PDF', 'Excel to PDF in CSharp', ]
categories: ['GroupDocs.Conversion Product Family']
---

Excel ([XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)) and [PDF](https://docs.fileformat.com/pdf/) files are among those document formats that are widely used in almost every business. For such commonly used files, there are many scenarios in which we need to convert one file into another format. In this article, we will learn different ways for how to convert Excel spreadsheets into PDF format using C# with .NET applications.



{{< figure align=center src="images/excel-to-pdf-in-csharp.jpg" alt="Convert Excel Spreadsheet to PDF using C#">}}


*   [.NET API for Excel Files to PDF Conversion](#excel-conversion-dotnet-api)
*   [Excel Sheets to PDF Conversion](#excel-to-pdf)
*   [Sequence of Excel Sheets to PDF Conversion](#sheets-sequence-to-pdf)
*   [Specific List of Excel Sheets to PDF Conversion](#list-of-sheets-to-pdf)
*   [Convert Selected Cell Range from Excel Sheet to PDF](#cell-ranges-to-pdf)

## .NET API for Excel Files to PDF Conversion {#excel-conversion-dotnet-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) provides APIs that allow the Excel files converted to PDF format within .NET applications. In this article, we will use [GroupDocs.Conversion for .NET](https://products.groupdocs.com/conversion/net/) to convert the Excel XLS/XLSX files data into PDF format. Additionally, the API supports the conversion of many other file formats like word-processing documents, spreadsheets, presentations, eBooks, images, etc that are mentioned in the [documentation](https://docs.groupdocs.com/conversion/net/supported-document-formats/).

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/conversion) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.conversion).

```
PM> Install-Package GroupDocs.Conversion
```

## Convert Excel Sheets to PDF - C# {#excel-to-pdf}

The following steps convert the complete workbook (all sheets) to PDF format using C#.

*   Prepare the **loading options** using the [SpreadsheetLoadOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.load/spreadsheetloadoptions).
*   **Load the Excel** spreadsheet using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter).
*   Call the [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions) to **convert** all the sheets and save to PDF format.

The following is the C# source code for how to convert the complete Excel workbook to PDF within the .NET application.

{{< gist GroupDocsGists 9f28fd2d21f1593ba5d55cc9bb7faa36 "ConvertExcelToPDF.cs" >}}



{{< figure align=center src="images/Converted-Excel-to-PDF.png" alt="Convert PDF from Excel Data">}}


## Sequence of Excel Sheets Conversion to PDF - C# {#sheets-sequence-to-pdf}

It is not always needed to transform the complete workbook. We can also convert any consecutive number of sheets. The following are the steps to convert any sub-sequence of the Excel workbook sheet(s) into PDF format using C#.

*   **Load** the Excel file using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter).
*   Define the **conversion options** using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions).
*   Set the **starting sheet number** and number of further sheets in **sequence**.
*   Call the [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method with the **conversion** options to get the subset of sheets in sequence saved in PDF format.

The following is the C# source code that converts the sheets in sequence, i.e. sheet numbers **2,3, and 4** to PDF within the .NET application.

{{< gist GroupDocsGists 9f28fd2d21f1593ba5d55cc9bb7faa36 "ConvertSheetSequenceToPDF.cs" >}}

## Specific Excel Sheets to PDF Conversion - C# {#list-of-sheets-to-pdf}

We can simply provide the list of the sheet numbers for the conversion of specific sheets. The following are the steps for how to convert any specific list of sheet numbers into PDF format using C#.

*   **Load** the spreadsheet file using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter).
*   **Select the sheets numbers** and set as list using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions).
*   Call the [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method with the conversion options to **convert** the listed sheets into PDF format.

The following C# code snippet converts sheet numbers **1, 3, and 5** to PDF within the .NET application.

{{< gist GroupDocsGists 9f28fd2d21f1593ba5d55cc9bb7faa36 "ConvertSpecifiedSheetsToPDF.cs" >}}

## Convert the Selected Cell Range of Excel Sheet to PDF - C# {#cell-ranges-to-pdf}

Last but not least, in fact, the most tricky one, we can also convert any cell range of Excel sheet(s) in almost a similar way as other approaches. The following are the steps to convert any cell range of workbook sheet(s) into PDF format using C#.

*   Firstly, define the **cell range** for conversion using the [SpreadsheetLoadOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.load/spreadsheetloadoptions).
*   **Load** the spreadsheet file using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter).
*   **Select the sheets** either by exact sheet numbers or sub-sequence using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions).
*   Call the [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method with the conversion options to **convert** the selected cell range of selected sheets into PDF format.

The following code converts the cell range (A1:C20) of sheet numbers 2, 3, and 4 to PDF format using C#.

{{< gist GroupDocsGists 9f28fd2d21f1593ba5d55cc9bb7faa36 "ConvertExcelSheetRangeToPDF.cs" >}}

## Conclusion

To conclude, we learned different ways to convert Excel spreadsheets into PDF format using C#. Firstly, we looked to convert the complete workbook into PDF format, then we converted the sub-sequence of sheets. Later, we learned how to convert any sheet(s) by providing the list of exact sheet numbers, and lastly, we obtained the PDF file from the selected cell range of selected sheet(s).

Learn more about **GroupDocs.Conversion APIs** from the [documentation](https://docs.groupdocs.com/conversion). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert Excel Sheet to CSV and vice versa in C#](https://blog.groupdocs.com/2021/08/18/convert-excel-xls-xlsx-and-csv-in-csharp/)
*   [Watermark Excel Sheets using C#](https://blog.groupdocs.com/2021/11/04/watermark-excel-sheets-using-csharp/)
*   [Watermark PDF Files using C#](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/)
*   [Convert Documents to Excel (XLS, XLSX) in C#](https://blog.groupdocs.com/2021/04/13/convert-document-to-excel-xls-xlsx-in-csharp/)




