---
title: 'Convert Excel Spreadsheets to PDF in Java'
date: Sun, 21 Nov 2021 07:32:11 +0000
draft: false
url: /2021/11/21/convert-excel-spreadsheets-to-pdf-in-java/
author: 'Shoaib Khan'
summary: 'When we want to share the data in worksheets that do not require editing, we often convert such Excel workbooks or specific sheets to PDF format. In this article, we will learn **4 different ways of converting Excel spreadsheets into PDF format in Java** using the document conversion API.'
tags: ['Convert Excel in Java', 'Convert Excel to PDF', 'Convert Excel to PDF in Java', 'convert to PDF in java', 'Excel to PDF', 'Excel to PDF in Java', ]
categories: ['GroupDocs.Conversion Product Family']
---



{{< figure align=center src="images/excel-to-pdf-in-java.jpg" alt="Convert Excel Spreadsheet to PDF in Java">}}


When we want to share the data in worksheets that do not require editing, we often convert such Excel workbooks or specific sheets to PDF format. In this article, we will learn **4 different ways of converting Excel spreadsheets into PDF format in Java** using the document conversion API.

Each conversion approach can be adopted with a little change in the code while loading the spreadsheets or with some tweaks in conversion options of the PDF format. Some of the possible ways to convert the spreadsheets in the article are as follows.

*   [Java API for Excel Files to PDF Conversion](#excel-conversion-java-api)
*   [Convert All Sheets to PDF](#excel-to-pdf)
*   [Continuous Number of Excel Sheets to PDF Conversion](#successive-sheets-to-pdf)
*   [Specific List of Excel Sheets to PDF Conversion](#list-of-sheets-to-pdf)
*   [Convert Selected Cell Range from Excel Sheet to PDF](#cell-ranges-to-pdf)

## Java API for Converting Excel Files to PDF {#excel-conversion-java-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) provides Java API that allows the many Excel file-formats including XLS, XLSX to convert into PDF format. In this article, we will use its [GroupDocs.Conversion for Java](https://products.groupdocs.com/conversion/java/). In addition to spreadsheets, the API supports the conversion of word-processing documents, presentations, eBooks, images, etc that are mentioned in the [documentation](https://docs.groupdocs.com/conversion/java/supported-document-formats/).

You can download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/conversion) or use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-conversion) configurations within your Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-conversion</artifactId>
        <version>21.10</version> 
</dependency>
```

## Convert All Sheets of Excel Files to PDF - Java {#excel-to-pdf}

The simplest way is to convert all the sheets to PDF format. The following steps convert the complete workbook (all sheets) to PDF format in Java.

*   **Load the Excel** (XLS, XLSX) workbook using [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter).
*   Convert it to PDF format using any of the overloaded [convert()](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter#convert(java.lang.String,%20com.groupdocs.conversion.options.convert.ConvertOptions)) methods using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/PdfConvertOptions).

The following are the 2 lines of Java source code that convert the complete Excel workbook to PDF.

{{< gist GroupDocsGists 98212012f8ebdca9891092e613998f76 "ConvertExcelToPDF.java" >}}



{{< figure align=center src="images/Converted-Excel-to-PDF.png" alt="Convert PDF from Excel Data">}}


## Successive Excel Sheets Conversion to PDF - Java {#successive-sheets-to-pdf}

If you are interested in extracting the subset of spreadsheets in sequence, you can easily do it by providing starting sheet number and the number of successive sheets. The following are the steps to convert any sub-sequence of the Excel workbook sheet(s) into PDF format in Java.

*   **Load** the spreadsheet using the [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter).
*   Define the **PDF conversion options** using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/PdfConvertOptions).
*   Set the **starting sheet number** and the **count of subsequent sheets**.
*   **Convert** the selected sheets into PDF according the settings using [convert()](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter#convert(java.lang.String,%20com.groupdocs.conversion.options.convert.ConvertOptions)) method.

The following is the Java code snippet that converts the first two sheets to PDF. (Sheet numbers **1 and 2**)

{{< gist GroupDocsGists 98212012f8ebdca9891092e613998f76 "ConvertSheetSequenceToPDF.java" >}}

## Specific Excel Sheets to PDF Conversion - Java {#list-of-sheets-to-pdf}

If you are thinking to convert random sheets (like sheet numbers 1, 2, 4, 7, ...), you can simply provide the exact sheet numbers as a list while converting. The following are the steps for converting any specific list of sheet numbers into PDF format in Java.

*   **Load** the Excel file using the [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter).
*   **Provide the exact sheets numbers** as a list using [PdfConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/PdfConvertOptions).
*   **Convert** the listed sheets into PDF format using the [convert()](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter#convert(java.lang.String,%20com.groupdocs.conversion.options.convert.ConvertOptions)) method.

The following code snippet converts the sheet numbers **1 and 3** to PDF format.

{{< gist GroupDocsGists 98212012f8ebdca9891092e613998f76 "ConvertSpecifiedSheetsToPDF.java" >}}

## Convert the Cell Range of Excel Sheet to PDF - Java {#cell-ranges-to-pdf}

Here is the unusual way to convert any segment of the spreadsheet(s). We can convert any cell ranges of Excel sheet(s) in almost a similar way as other approaches discussed above. The following are the steps for converting the cell range of workbook sheet(s) into PDF format in Java.

*   Define the **cell range** of the sheets.
*   **Load** the spreadsheet file.
*   **Select the sheets** either by providing successive sheets range or the exact sheet numbers.
*   **Convert** the sheets into PDF format according to settings.

The following code converts the cell range (A1:C20) of sheet number 1 to PDF format in Java.

{{< gist GroupDocsGists 98212012f8ebdca9891092e613998f76 "ConvertExcelSheetRangeToPDF.java" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

Let's sum up what we learned today. We learned four different ways for converting Excel spreadsheets into PDF format in Java using GroupDocs.Conversion. Initially, we converted the complete workbook into PDF format, then the consecutive sheets. Next, multiple sheets were changed to PDF by listing their exact sheet numbers. Finally, we obtained the PDF file from the selected cell range of the selected sheet(s).

Learn more about **GroupDocs.Conversion APIs** from the [documentation](https://docs.groupdocs.com/conversion). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert CSV and Excel (XLS XLSX) in Java](https://blog.groupdocs.com/2021/07/31/convert-csv-and-excel-xls-xlsx-in-java/)
*   [Convert Documents to Excel (XLS, XLSX) in Java](https://blog.groupdocs.com/2021/05/22/convert-documents-to-excel-xls-xlsx-in-java/)
*   [Watermark Excel Sheets in Java](https://blog.groupdocs.com/2021/11/10/watermark-excel-sheets-in-java/)
*   [Watermark PDF Files in Java](https://blog.groupdocs.com/2021/06/26/add-watermark-to-pdf-in-java/)




