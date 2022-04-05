---
title: 'Convert Source Code to PDF in Java'
date: Thu, 16 Dec 2021 16:44:27 +0000
draft: false
url: /2021/12/16/convert-source-code-to-pdf-in-java/
author: 'Shoaib Khan'
summary: 'If you want to share your code snippets, you can convert them into PDF format. In this article, we will discuss **how to convert Java, Python, C++, PHP source code to PDF** format within Java application. Additionally, we will also learn to password-protect the converted PDF files.

The following topics are discussed in this article:

*   Source Code Conversion Java API
*   Java to PDF using Java
*   Python to PDF using Java
*   PHP to PDF - Protect the PDF file'
tags: ['Convert Source Code to PDF in Java', 'Java to PDF', 'PHP to PDF', 'Python Code to PDF', 'Source Code to PDF']
categories: ['GroupDocs.Viewer Product Family']
---

If you want to share your code snippets, you can convert them into PDF format. In order to do this, we will discuss **how to convert Java, PHP, Python, **C#, C++** source code to PDF** format within Java application. Additionally, we will also learn to password-protect the converted PDF files.



{{< figure align=center src="images/convert-source-code-to-pdf-in-java.jpg" alt="Convert Source Code to PDF">}}


The following topics are discussed below:

*   [Source Code Conversion Java API](#source-code-converter-java-api)
*   [Java to PDF using Java](#java-to-pdf)
*   [Python to PDF using Java](#python-to-pdf)
*   [PHP to PDF - Protect the PDF file](#php-to-pdf)

## Source Code Converter Java API {#source-code-converter-java-api}

[GroupDocs.Viewer](https://products.groupdocs.com/viewer/) provides Java API to [render files into different formats](https://docs.groupdocs.com/viewer/java/supported-document-formats/) like PDF, HTML, and image formats. I will use this API to convert source code files of different languages into PDF format.

You can download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/viewer) or use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs) configurations within your Java applications.

```
<repository>
	<id>GroupDocsArtifactRepository</id>
	<name>GroupDocs Artifact Repository</name>
	<url>https://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-viewer</artifactId>
        <version>21.11</version> 
</dependency>
```

## Convert Java Code to PDF {#java-to-pdf}

Let's quickly come to the objective and see the results. The following steps allow you to convert the Java source code file to PDF.

*   Load the Java file using the [Viewer](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer/Viewer) class.
*   Define the output file and options using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer.options/PdfViewOptions) class.
*   Convert the loaded Java file to PDF using the appropriate [view()](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer/Viewer#view(com.groupdocs.viewer.options.ViewOptions)) method.

The following Java code snippet converts the complete Java source code file to PDF format.

{{< gist GroupDocsGists 07263be03154d33914f5671e6254513f "JavaToPdf.java" >}}

Here is the converted PDF of the Java file using the above Java code. If you want to add security to the resultant PDF file, jump to the section below where the [PHP file gets converted](#php-to-pdf).



{{< figure align=center src="images/java-to-pdf.jpg" alt="Java source file converted to PDF">}}


## Convert Python Code to PDF using Java {#python-to-pdf}

Do you really think, there will be a separate code for converting the Python code to PDF and it will be somewhat different from converting a Java file? No, it's the same, just hand over the right .py file. The following steps allow you to convert the Python code to PDF.

*   Load the Python file using the [Viewer](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer/Viewer) class.
*   Set the output file path and options using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer.options/PdfViewOptions) class.
*   Convert the loaded .py file to PDF using the suitable [view()](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer/Viewer#view(com.groupdocs.viewer.options.ViewOptions)) method.

The following Java code snippet converts the complete Python source code file into PDF format.

{{< gist GroupDocsGists 07263be03154d33914f5671e6254513f "PythonToPdf.java" >}}

## Convert PHP to PDF using Java {#php-to-pdf}

Similarly, you can also convert the PHP files. One more thing to add here; while converting your source code files, you can add security to the PDF files. Let's protect the PHP code when it is converted to PDF format. The following steps show how to convert the PHP file to PDF.

*   Load the PHP file using the [Viewer](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer/Viewer) class.
*   Define the security using [Security](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer.options/Security) class.
*   Set the passwords for opening and editing the resultant PDF file.
*   Define the output file and its options using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer.options/PdfViewOptions) class.
*   Call the [view()](https://apireference.groupdocs.com/viewer/java/com.groupdocs.viewer/Viewer#view(com.groupdocs.viewer.options.ViewOptions)) method to render the loaded PHP file to the protected PDF.

The following Java code example converts the PHP source code file to a password-protected PDF file.

{{< gist GroupDocsGists 07263be03154d33914f5671e6254513f "PhpToPdfProtected.java" >}}

Similarly, you can use this code for other source codes of [supported programming languages](https://docs.groupdocs.com/viewer/java/supported-document-formats/) like C#, C/C++, GROOVY, Ruby, and more.

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To conclude, we learned to convert source code files of different programming languages to PDF format using Java. We converted the Java, Python, and PHP files into PDF format. Additionally, we learned how to password-protect the resultant PDF file. Using this API, you can start building your own source code viewer Java application.

To learn more about **GroupDocs.Viewer**, visit the [documentation](https://docs.groupdocs.com/viewer). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Convert Images to PDF in Java](https://blog.groupdocs.com/2021/04/21/convert-images-to-pdf-in-java/)
*   [Convert Excel Sheets to PDF in Java](https://blog.groupdocs.com/2021/11/21/convert-excel-spreadsheets-to-pdf-in-java/)
*   [View Word Documents as Responsive HTML Page using Java](https://blog.groupdocs.com/2021/09/23/view-word-documents-as-responsive-html-page-using-java/)




