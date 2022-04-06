---
title: 'Convert MSG and EML files to PDF in Java'
date: Wed, 02 Sep 2020 14:04:02 +0000
draft: false
url: /2020/09/02/convert-msg-and-eml-files-to-pdf-in-java/
author: 'Shoaib Khan'
summary: 'Emails to PDF conversions are often required for referencing and requirements like sharing the email content. In this article, we will learn about **how to convert email message files like MSG and EML into PDF using Java**. Previously, in one of the [earlier blog posts](https://blog.groupdocs.com/2019/12/06/convert-eml-or-msg-file-to-pdf-in-csharp/), we have already learned to convert MSG & EML files using C# in .NET application. This will help to automate the Email conversion within the desktop or web applications.'
tags: ['convert emails to pdf', 'Convert MSG or EML to PDF in Java', 'eml to pdf in java', 'MSG to PDF in Java']
categories: ['GroupDocs.Conversion Product Family']
---



{{< figure align=center src="images/Convert-Emails-to-PDF-in-Java.png" alt="Convert Emails to PDF in Java">}}


Emails to PDF conversions are often required for referencing and requirements like sharing the email content. In this article, we will learn about **how to convert email message files like MSG and EML into PDF using Java**. Previously, in one of the [earlier blog posts](https://blog.groupdocs.com/2019/12/06/convert-eml-or-msg-file-to-pdf-in-csharp/), we have already learned to convert MSG & EML files using C# in .NET application. This will help to automate the Email conversion within the desktop or web applications.

The following are the topics covered in this article:

*   [Java Conversion Library](https://blog.groupdocs.com/2020/09/02/convert-msg-and-eml-files-to-pdf-in-java/#java-conversion-library)
*   [Conversion of MSG to PDF using Java](https://blog.groupdocs.com/2020/09/02/convert-msg-and-eml-files-to-pdf-in-java/#convert-msg-to-pdf-in-java)
*   [Conversion of EML to PDF using Java](https://blog.groupdocs.com/2020/09/02/convert-msg-and-eml-files-to-pdf-in-java/#convert-eml-to-pdf-in-java)

## Java Conversion Library {#java-conversion-library}

In this article, I will be using [GroupDocs.Conversion for Java](https://products.groupdocs.com/conversion/java) API for the conversions. By using it, you may convert email document formats like MSG and EML to PDF and other formats without losing the email format.

You may get the JAR file from the [downloads](https://downloads.groupdocs.com/conversion/java) section. For the maven based applications, following is the pom.xml configuration:

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
        <version>20.6</version> 
</dependency>
```

## Convert MSG to PDF using Java {#convert-msg-to-pdf-in-java}

The following are the steps to convert the Outlook MSG files to PDF with just a few lines of code. Embedded links in the steps will allow further exploring the classes and methods.

1.  Create an instance of the [Converter](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion/Converter) class and pass the MSG file to the constructor.
2.  Instantiate the [PdfConvertOptions](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion.options.convert/PdfConvertOptions) class.
3.  Call [convert](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion/Converter#convert(java.lang.String,%20com.groupdocs.conversion.options.convert.ConvertOptions)) method to get the converted PDF file.

{{< gist GroupDocsGists 26a955193719a219fd8db89eb6de7516 "ConvertMsgToPdf.java" >}}

Here is the sample MSG file that is created using Microsoft Outlook. Further below is the PDF file, that is obtained by converting the MSG file using the above-mentioned java code.



{{< figure align=center src="images/MSG-message.png" alt="MSG file to be converted to PDF" caption="MSG file">}}




{{< figure align=center src="images/converted-msg-to-pdf-in-java.png" alt="Converted PDF file from MSG" caption="PDF file converted from MSG format using the above Java code.">}}


## Convert EML to PDF using Java {#convert-eml-to-pdf-in-java}

We can programmatically convert our email messages stored in EML format, into PDF format with similar lines of java code very easily and efficiently. The following steps will guide to achieve the objective.

1.  Initialize the [Converter](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion/Converter) object providing the source EML file path.
2.  Initialize the [PDFConvertOptions](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion.options.convert/PdfConvertOptions). You may set further customization for the resultant PDF file.
3.  Just call the [convert](https://apireference.groupdocs.com/java/conversion/com.groupdocs.conversion/Converter#convert(java.lang.String,%20com.groupdocs.conversion.options.convert.ConvertOptions)) method of the Converter class and pass it the resultant PDF file path and the already set PDFConvertOptions as parameters.

{{< gist GroupDocsGists 26a955193719a219fd8db89eb6de7516 "ConvertEmlToPdf.java" >}}

Shown below are the source EML file and the converted PDF file screenshots, that has been converted using the above java code.



{{< figure align=center src="images/EML-message.png" alt="EML file to be converted to PDF" caption="EML file">}}




{{< figure align=center src="images/converted-eml-to-pdf-in-java.png" alt="Converted PDF file from EML" caption="PDF file converted from EML format using Java.">}}


## Conclusion

In this article, we learned how to convert the MSG and EML files to PDF using Java Conversion API. Furthermore, we can programmatically apply customization on PDF files to get the outcome in our desired style. You may get some more about GroupDocs.Conversion for Java from the documentation.

## See Also

*   [Convert EML or MSG file to PDF in C#](https://blog.groupdocs.com/2019/12/06/convert-eml-or-msg-file-to-pdf-in-csharp/)




