---
title: 'Convert CSV to Excel (XLS XLSX) &amp; Vice Versa in Java'
date: Sat, 31 Jul 2021 04:07:00 +0000
draft: false
url: /2021/07/31/convert-csv-and-excel-xls-xlsx-in-java/
author: 'Shoaib Khan'
summary: '**CSV** contains the comma-separated values, normally used to store tabular data without formatting. These files can be viewed in any text editor and also in MS Excel for tabular format. On the other hand, the most used formats for MS Excel files are XLS and XLSX. These formats support countless formatting options. This article discusses the conversion of the Excel spreadsheets of **XLS/XLSX format to CSV** format and **CSV to XLS/XLSX **format programmatically **using Java**.'
tags: ['Convert XLS and CSV in Java', 'CSV to Excel in Java', 'CSV to XLS in Java', 'CSV to XLSX in Java', 'Excel to CSV in Java', 'XLS to CSV in Java', 'XLSX to CSV in Java']
categories: ['GroupDocs.Conversion Product Family']
---



{{< figure align=center src="images/convert-csv-and-xls-xlsx-in-java.jpg" alt="Convert to CSV and XLS XLSX in Java">}}


**CSV** contains the comma-separated values, normally used to store tabular data without formatting. These files can be viewed in any text editor and also in MS Excel for tabular format. On the other hand, the most used formats for MS Excel files are XLS and XLSX. These formats support countless formatting options. This article discusses the conversion of the Excel spreadsheets of **XLS/XLSX format to CSV** format and **CSV to XLS/XLSX **format programmatically **using Java**.

The following topics are covered below:

*   [Java API for XLS/XLSX and CSV Conversion](#excel-csv-java-api)
*   [Excel to CSV Conversion](#excel-to-csv)
*   [CSV to Excel Conversion](#csv-to-excel)

## Java API for Excel Files and CSV Conversion {#excel-csv-java-api}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion/) offers Java API that allows the conversion of spreadsheet formats into one another. I will be using this API for converting XLSX into CSV and also CSV into XLS or XLSX using Java. Additionally, the API allows the [back and forth conversion of many other document and image formats](https://docs.groupdocs.com/conversion/java/supported-document-formats/) like word-processing documents, presentations, eBooks, JPG, PNG, WebP, and many more.

### Download or Configure

You may download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/conversion), or just get the repository and dependency configurations for the pox.xml of your **maven-based** Java applications.

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
        <version>21.7</version> 
</dependency>
```

## Convert CSV to Excel (XLS/XLSX) in Java {#csv-to-excel}

Transformation of comma-separated data into the tabular form for a better presentation requires conversion from CSV to XLS/XLSX format. The following steps allow converting the CSV files to XLS/XLSX format within the Java application.

*   Prepare the load options for loading the CSV file.
*   Load the CSV using the [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter) class.
*   Set the conversion format to XLSX using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/SpreadsheetConvertOptions).
*   Call the **convert** method to get the CSV data transformed into XLSX format.

The following code shows how to convert your CSV file into XLSX format in Java.

{{< gist GroupDocsGists f76d26570da3a1c3781cde92da456683 "ConvertCsvToExcel.java" >}}

For the XLS format, just set the conversion format accordingly and provide the appropriate file name with the extension.

## Convert Excel (XLS/XLSX) to CSV in Java {#excel-to-csv}

Similarly, if formatting is not required, you can remove the styles and visuals and simply keep the comma-separated data by converting the XLS/XLSX to CSV format and saving the space.

The following steps allow converting the XLS or XLSX format to CSV within the Java applications.

*   Load the Excel file (XLS or XLSX) using the [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter) class.
*   Set the conversion format to CSV using [SpreadsheetConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/SpreadsheetConvertOptions).
*   Call the **convert** method to transform the spreadsheet data into CSV format.

The following code shows how to convert XLS or XLSX to CSV format in Java.

{{< gist GroupDocsGists f76d26570da3a1c3781cde92da456683 "ConvertExcelToCSV.java" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you learned how to convert the MS Excel files to CSV format and also the conversion of CSV files to XLS and XLSX format programmatically with your Java applications. You can learn more about the Java Conversion API using the [documentation](https://docs.groupdocs.com/conversion), or by examples available on [GitHub](https://github.com/groupdocs-conversion). Get in touch with us for any query at the [forum](https://forum.groupdocs.com/).

## See Also

*   [Generate Reports from CSV Data in Java](https://blog.groupdocs.com/2021/07/07/generate-reports-from-csv-data-in-java/)
*   [Create Reports from XML Data in Java](https://blog.groupdocs.com/2021/07/10/generate-reports-from-xml-data-in-java/)
*   [Convert Excel Spreadsheets to PDF in Java](https://blog.groupdocs.com/2021/11/21/convert-excel-spreadsheets-to-pdf-in-java/)
*   [Convert PDF, Word documents to Excel XLS, XLSX in Java](https://blog.groupdocs.com/2021/05/22/convert-documents-to-excel-xls-xlsx-in-java/)




