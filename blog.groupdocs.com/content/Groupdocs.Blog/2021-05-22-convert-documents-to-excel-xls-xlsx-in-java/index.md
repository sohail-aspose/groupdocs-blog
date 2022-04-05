---
title: 'Convert Documents to Excel XLS, XLSX in Java'
date: Sat, 22 May 2021 18:39:23 +0000
draft: false
url: /2021/05/22/convert-documents-to-excel-xls-xlsx-in-java/
author: 'Shoaib Khan'
summary: 'For the data in tabular form of your PDF and Word documents, you sometimes need to convert it to Excel spreadsheets. We need to automate this conversion of as many documents to spreadsheets or multiple workbooks. This article will discuss how to programmatically convert Word documents to Excel and also how to convert PDF files to Excel spreadsheets in Java.

The following are the topics discussed briefly in this article:

*   Java API - Documents to Spreadsheets Conversion
*   Convert PDF to Excel Spreadsheet
*   Convert Word to Excel Spreadsheet
*   PDF or Word to Spreadsheet conversion with more options

[Continue Reading ...](https://blog.groupdocs.com/2021/05/22/convert-documents-to-excel-xls-xlsx-in-java)'
tags: ['Convert to Excel in Java', 'DOC to XLS in Java', 'DOCX to XLSX in Java', 'PDF to Excel in Java', 'Word to Excel in Java']
categories: ['GroupDocs.Conversion Product Family']
---

For the data in tabular form of your PDF and Word documents, you sometimes need to convert it to Excel spreadsheets. We need to automate this conversion of as many documents to spreadsheets or multiple workbooks. This article will discuss how to programmatically convert Word documents to Excel and also how to convert PDF files to Excel spreadsheets in Java.



{{< figure align=center src="images/pdf-word-to-xls-in-java.jpg" alt="Convert Word and PDF to Excel in Java">}}


The following topics are discussed briefly here:

*   [Java API - Documents to Spreadsheets Conversion](#convert-to-spreadsheet-java-api)
*   [Convert PDF to Excel Spreadsheet](#pdf-to-excel-csharp)
*   [Convert Word to Excel Spreadsheet](#word-to-excel-csharp)
*   [PDF or Word to Spreadsheet conversion with more options](#pdf-word-to-excel-adv)

## Java API for Conversion to Spreadsheet {#convert-to-spreadsheet-java-api}

[GroupDocs.Conversion for Java](https://products.groupdocs.com/conversion/net) is the API that allows you to convert PDF and Word documents to spreadsheets within your Java applications. The API allows document and image conversions in many file formats. Some of the supported document formats include word-processing documents, spreadsheets, presentations, eBooks, AutoCAD formats, PDF, email messages, Web pages, images.

### Download and Configure

You can get the conversion library from the downloads section or add the following pom.xml configuration in your Maven-based Java application. Afterward, you can try examples of this article as well as many more examples available on [GitHub](https://github.com/groupdocs-conversion). For the details, you may visit the [API Reference](https://apireference.groupdocs.com/conversion/java).

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-conversion</artifactId>
        <version>21.4</version> 
</dependency>
```

## Convert PDF to Excel in Java {#pdf-to-excel-csharp}

The following steps can be followed to convert any PDF document to an Excel spreadsheet.

*   Load the PDF file using [Converter](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion/Converter) class.
*   Prepare convert options using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/SpreadsheetConvertOptions).
*   Call the [convert](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter#convert(java.io.OutputStream,%20com.groupdocs.conversion.contracts.ConvertedDocumentStream,%20com.groupdocs.conversion.options.convert.ConvertOptions)) method with the created options.

The following code sample shows how to convert a PDF file into an Excel XLSX spreadsheet in Java.

{{< gist GroupDocsGists c54011c23506f561da98126b8307f13c "ConvertPdfToExcel.java" >}}

## Convert Word to Excel in Java {#word-to-excel-csharp}

Similarly, any Word document can be converted to an Excel spreadsheet in the same manner as we just converted the PDF document. Provide the right source file and get it converted into XLS or XLSX.

The following are the step to convert any DOC DOCX file to an Excel spreadsheet.

*   Load the DOC, DOCX file using Converter class.
*   Prepare the convert options using SpreadsheetConvertOptions.
*   Call the convert method of the Converter class with options.

The following source code shows how to convert a DOC or DOCX file into Excel XLSX format in Java.

{{< gist GroupDocsGists c54011c23506f561da98126b8307f13c "ConvertWordToExcel.java" >}}

## PDF or Word to Spreadsheet Conversion with more options using Java {#pdf-word-to-excel-adv}

You are not bound to get the whole document converted every time. You can convert just the selected pages of your document. The API gives you the privilege to convert the document with various options that include:

*   Starting **Page Number**.
*   **Page Count**.
*   **Specific Pages** for conversion.
*   **Format** to convert into.
*   **Password** for make the file protected.
*   **Zoom** to make it large or smaller.
*   **Watermark** on the converter file.

The following are the steps for how to convert some of the pages of a PDF file into XLSX format with different zoom in Java.

{{< gist GroupDocsGists c54011c23506f561da98126b8307f13c "ConvertPdfToExcelAdv.java" >}}

The PDF file and the converted spreadsheet as output are shown here. It converted the second page of the PDF file into XLSX format.



{{< figure align=center src="images/pdf-to-xls-in-csharp.jpg" alt="Convert PDF to Excel XLS XLSX Programmatically">}}


## Get a Free API License {#Get-a-Free-API-License}

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without evaluation limitations.

## Conclusion

In this article, we discussed the conversion of PDF and Word documents to an Excel spreadsheet in Java. Additionally, we learned how to convert any part of the document with options like watermark, zoom, and make it protected using password protection.

For more options and examples, visit the [documentation](https://docs.groupdocs.com/conversion) and the [GitHub](https://github.com/groupdocs-conversion) repository. For queries, reach us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Images to PDF in Java](https://blog.groupdocs.com/2021/04/21/convert-images-to-pdf-in-java/)
*   [Spreadsheets to PDF in Java](https://blog.groupdocs.com/2021/11/21/convert-excel-spreadsheets-to-pdf-in-java/)
*   [Presentations to PDF in Java](https://blog.groupdocs.com/2021/02/15/convert-presentations-odp-pptx-ppt-to-pdf-in-java/)
*   [CAD Drawings to PDF in Java](https://blog.groupdocs.com/2020/10/31/convert-cad-drawings-to-pdf-in-java/)




