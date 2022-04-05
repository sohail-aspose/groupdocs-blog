---
title: 'Watermark Excel Sheets in Java'
date: Wed, 10 Nov 2021 14:04:00 +0000
draft: false
url: /2021/11/10/watermark-excel-sheets-in-java/
author: 'Shoaib Khan'
summary: 'Watermarks can be added to the documents either to protect the document from piracy, or to show any sumbol or message. In other posts, we discussed ways to watermark different [documents](https://blog.groupdocs.com/2021/06/26/add-watermark-to-pdf-in-java/), [images](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/), and [presentations](https://blog.groupdocs.com/2021/06/09/watermark-presentation-slides-using-java/). In this article, you will learn **how to add watermark to Excel workbooks in different ways in Java**. We will be applyling watermarks separately using each approach.

The following topics are covered in this article:

*   Watermarking API for Java
*   Add **Text Watermark** to Excel Sheets
*   Apply Watermark to **Specific Excel Sheet**
*   Add Watermark to Excel Sheet **as Background**'
tags: ['add watermark in java', 'how to add watermark in Java', 'watermark excel', 'watermark excel sheets in Java', 'watermarking API for Java']
categories: ['GroupDocs.Watermark Product Family']
---



{{< figure align=center src="images/add-watermark-to-excel-in-java.jpg" alt="Add Watermark to Excel Sheet in Java">}}


Watermarks can be added to the documents either to protect the document from piracy or to show any symbol or message. In other posts, we discussed ways to watermark different documents, images, and presentations. In this article, you will learn how to add watermark to Excel workbooks in different ways in Java. We will be applying watermarks separately using each approach.

The following topics are covered below:

*   [Watermarking API for Java](#watermarking-java-api)
*   [Add **Text Watermark** to Excel Sheets](#watermark-all-sheets)
*   [Apply Watermark to **Specific Excel Sheet**](#watermark-any-sheet)
*   [Add Watermark to Excel Sheet **as Background**](#watermark-sheet-as-background)

## Java API to Watermark Excel Sheets {#watermarking-java-api}

[GroupDocs.Watermark for Java](https://products.groupdocs.com/watermark/) is the API to automate the watermarks for documents, presentations, images, and many other file formats. The complete list of supported document formats is available in the [documentation](https://docs.groupdocs.com/watermark/java/supported-document-formats/).

You can download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/watermark) or use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-watermark) configurations within your Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>https://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-watermark</artifactId>
        <version>21.3</version> 
</dependency>
```

## Watermark Excel Sheets using Java {#watermark-all-sheets}

The watermarking API provides customization while inserting the watermark to the spreadsheets as a text. The following are the steps to add watermarks to Excel workbooks in Java.

*   Load the source spreadsheet using [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker) and the [SpreadsheetLoadOptions](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.options/SpreadsheetLoadOptions).
*   Define the watermark text and appearance properties using [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark).
*   Add the defined watermark to the Excel worksheet using [add()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) mehtod.
*   Save the resultant spreadsheet with watermark using the [save()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String)) method.

The following Java code sample adds the text watermark to all the sheets of the Excel workbook with rotation and opacity and the set alignment.

{{< gist GroupDocsGists a8ff600a6d3b7460f52abe2836bffe0a "AddWatermarkToAllSheets.java" >}}

## Watermark Specific Excel Sheet using Java {#watermark-any-sheet}

Likewise, you can also insert watermarks into any single sheet of the workbook. The following steps guide on how to apply text watermark to the specific sheet of the Excel workbook in Java.

*   Load the spreadsheet using the [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker).
*   Set the watermark appearance and text using the [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark).
*   Set the worksheet index so that watermark is applied to the mentioned sheet only.
*   Add the text watermark to the Excel worksheet using [add()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) mehtod with watermarking options.
*   Save the output spreadsheet having the watermark using the [save()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String)) method.

The following Java code snippet applies the text watermark to only the mentioned sheet of the Excel workbook.

{{< gist GroupDocsGists a8ff600a6d3b7460f52abe2836bffe0a "AddWatermarkToSpecificSheet.java" >}}

## Watermark Excel Sheets as Background using Java {#watermark-sheet-as-background}

Likewise, we can also add watermarks as the background of the spreadsheet. There will be some modification to the above approach to applying watermarks. The following are the steps that insert background text watermark to Excel spreadsheet in Java.

*   Load the spreadsheet using [Watermarker](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker).
*   Prepare the watermark text and its appearance using [TextWatermark](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark.watermarks/TextWatermark).
*   Set the watermark settings to make it as background using watermarking options by getting content and setting dimensions.
*   Add the watermark to the workbook sheets using the [add()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#add(com.groupdocs.watermark.Watermark)) mehtod.
*   Lastly, save the watermarked spreadsheet using the [save()](https://apireference.groupdocs.com/watermark/java/com.groupdocs.watermark/Watermarker#save(java.lang.String)) method.

The following code sample can be used to add a background text watermark to an Excel spreadsheet in Java.

{{< gist GroupDocsGists a8ff600a6d3b7460f52abe2836bffe0a "AddWatermarkToExcelAsBackground.java" >}}



{{< figure align=center src="images/watermark-excel-sheets-programmatically.png" alt="Watermark Excel Sheets Programmatically">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

In this article, we discussed that how we can add watermarks to the excel sheets in different ways within the Java application. We learned to insert text watermark to all the sheets of the Excel workbook, and then we applied the watermark to the specific sheet only. Later, we applied the watermark as a background. You can now use this feature and build your own application to watermark spreadsheets.

Learn more about the API from the [documentation](https://docs.groupdocs.com/watermark). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Watermark Excel Sheets using C#](https://blog.groupdocs.com/2021/11/04/watermark-excel-sheets-using-csharp/)
*   [Watermark PDF Files in Java](https://blog.groupdocs.com/2021/06/26/add-watermark-to-pdf-in-java/)
*   [Add Watermark to Images in Java](https://blog.groupdocs.com/2020/09/15/add-watermark-to-images-in-java/)
*   [Watermark Presentation Slides using Java](https://blog.groupdocs.com/2021/06/09/watermark-presentation-slides-using-java/)
*   [Find and Remove Watermarks from Documents in Java](https://blog.groupdocs.com/2020/11/30/find-and-remove-watermarks-from-documents-in-java/)




