---
title: 'Watermark Excel Sheets using C#'
date: Thu, 04 Nov 2021 18:46:00 +0000
draft: false
url: /2021/11/04/watermark-excel-sheets-using-csharp/
author: 'Shoaib Khan'
summary: 'We have already discussed ways to watermark different [documents](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/), [images](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/), and [presentations](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/). Today, we will be discussing how to add watermark to an Excel workbook in different ways using C# with the .NET application.

The following topics are covered in this article:

*   Add **Text Watermark** to Excel Sheet
*   Apply Watermark to **Specific Excel Sheet**
*   Add Watermark to Excel Sheet **as Background**'
tags: ['add watermark in csharp', 'how to add watermark in csharp', 'watermark dotnet api', 'watermark excel', 'watermark excel sheets in csharp']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/add-watermark-to-excel-using-csharp.jpg" alt="Add Watermark to Excel Sheet using C#">}}


We have already discussed ways to watermark different [documents](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/), [images](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/), and [presentations](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/). Today, we will be discussing how to add watermark to an Excel workbook in different ways using C# with the .NET application.

The following topics are covered below:

*   [Watermarking API for .NET](#watermarking-dotnet-api)
*   [Add **Text Watermark** to Excel Sheets](#watermark-all-sheets)
*   [Apply Watermark to **Specific Excel Sheet**](#watermark-any-sheet)
*   [Add Watermark to Excel Sheet **as Background**](#watermark-sheet-as-background)

## .NET API to Watermark Excel Sheets {#watermarking-dotnet-api}

[GroupDocs.Watermark](https://products.groupdocs.com/watermark/) provides the .NET API for documents and images of various file formats. We will use [GroupDocs.Watermark for .NET](https://products.groupdocs.com/watermark/net/) to apply watermarks in spreadsheets in different ways using C#.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/watermark/net) or get it from [NuGet](https://www.nuget.org/packages/GroupDocs.Watermark/).

```
Install-Package GroupDocs.Watermark
```

## Watermark Excel Sheets using C# {#watermark-all-sheets}

The API allows you to insert text to the spreadsheets as a watermark with different customizations. The following are the steps to add a watermark to Excel workbooks using C# with the .NET applications.

*   Prepare the loading options for spreadsheet.
*   Load the spreadsheet using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker).
*   Define the watermark text and appearance using [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark).
*   Add the text watermark to the Excel worksheet using [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) mehtod.
*   Save the resultant spreadsheet with watermark using the [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following C# code sample applies the text watermark to all the sheets of the Excel workbook with rotation and opacity.

{{< gist GroupDocsGists 9d8b16b89e156aa787fe6c19c4db8ef4 "AddWatermarkToAllSheets.cs" >}}

## Watermark Specific Excel Sheet using C# {#watermark-any-sheet}

Similarly, you can apply watermarks to any specific sheet only instead of applying them to all the sheets of the workbook. The following steps guide on how to insert text watermark to the specific sheet of the Excel workbook using C#.

*   Prepare the loading options.
*   Load the spreadsheet using the [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker) class.
*   Define the watermark appearance and text using the [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark) class.
*   Set the worksheet index so that watermark is applied to the mentioned sheet only.
*   Add the text watermark to the Excel worksheet using [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) mehtod with watermarking options.
*   Save the output spreadsheet having the watermark using the [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following code snippet applies the text watermark to only the mentioned sheet of the Excel workbook.

{{< gist GroupDocsGists 9d8b16b89e156aa787fe6c19c4db8ef4 "AddWatermarkToSpecificSheet.cs" >}}

## Watermark Excel Sheets as Background using C# {#watermark-sheet-as-background}

Likewise, we can also add watermarks as the background of the spreadsheet. There will be a little change from the above techniques of applying watermarks. The following are the steps that allow inserting background text watermark to Excel spreadsheet using C#.

*   Prepare the loading options for loading spreadsheet.
*   Load the spreadsheet using [Watermarker](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker).
*   Define the watermark text and appearance (rotation, position, dimensions, opacity, color, and more) using [TextWatermark](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark.watermarks/textwatermark).
*   Set the background watermarking options by getting content and setting dimensions.
*   Set the index of worksheet to apply watermark. (Optional)
*   Add the watermark to the spreadsheet using [Add](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/add/index) mehtod.
*   Save the spreadsheet with watermark using the [Save](https://apireference.groupdocs.com/watermark/net/groupdocs.watermark/watermarker/methods/save/index) method.

The following code sample shows how to add a background watermark to an Excel spreadsheet using C# within the .NET application.

{{< gist GroupDocsGists 9d8b16b89e156aa787fe6c19c4db8ef4 "AddWatermarkToExcelAsBackground.cs" >}}



{{< figure align=center src="images/watermark-excel-sheets-programmatically.png" alt="Watermark Excel Sheets Programmatically">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, we discussed different ways to add watermark to excel sheets using C#. First, we added text watermarks to all the sheets of the Excel workbook. Then we applied the watermark to the specific sheet only. Lastly, we inserted the text-based watermark into the Excel workbook as a background.

Visit the product [documentation](https://docs.groupdocs.com/watermark) to learn more about the API. For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Watermark Excel Sheets in Java](https://blog.groupdocs.com/2021/11/10/watermark-excel-sheets-in-java/)
*   [Watermark PDF Files using C#](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/)
*   [Add Watermark to Presentation Slides using C#](https://blog.groupdocs.com/2021/05/01/add-watermark-to-presentations-using-csharp/)
*   [Watermark Images using C#](https://blog.groupdocs.com/2020/12/20/add-watermark-to-images-using-csharp-dotnet/)




