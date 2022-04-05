---
title: 'Extract ZIP Files Data in Java'
date: Wed, 08 Sep 2021 13:14:00 +0000
draft: false
url: /2021/09/08/extract-zip-files-data-in-java/
author: 'Shoaib Khan'
summary: 'ZIP Archives are one of the most popular and commonly used compressed file formats. The main reason for using ZIP files is to reduce the total file size and to send multiple files as a single archive. As a developer, you can extract the text, images, and even metadata from the files that are compressed within ZIP archives. In this article, we will discuss **how to extract the ZIP archives data in Java**.

The following topics are covered in this article:

*   Java API for ZIP files data extraction.
*   How to extract ZIP files data using Java.'
tags: ['Extract Archives in Java', 'Extract from ZIP', 'Extract from ZIP in Java', 'unzip data in Java']
categories: ['GroupDocs.Parser Product Family']
---

ZIP Archives are one of the most popular and commonly used compressed file formats. The main reason for using ZIP files is to reduce the total file size and to send multiple files as a single archive. As a developer, you can extract the text, images, and even metadata from the files that are compressed within ZIP archives. In this article, we will discuss **how to extract ZIP archives data in Java**.



{{< figure align=center src="images/extract-data-from-zip-files-in-java.jpg" alt="Extract data from ZIP files in Java">}}


The following topics are covered below:

*   [Java API for ZIP files data extraction.](#zip-files-data-extraction-java-api)
*   [How to extract ZIP files data using Java.](#how-to-extract-zip-data)
*   [Extract Images from Files within ZIP files in Java](#extract-images-from-zip-data)

## Java API to Extract ZIP files Data {#zip-files-data-extraction-java-api}

[GroupDocs.Parser](https://products.groupdocs.com/parser/) provides the document parsing solution for developers which also includes the Java API. I will be using this [Java API to extract ZIP files data](https://products.groupdocs.com/parser/java/) in the example(s) of this article. Additionally, this API allows data extraction of images, raw text, structured and formatted text, and metadata from a long list of [supported document formats](https://docs.groupdocs.com/parser/java/supported-document-formats/). These document formats include word-processing documents, PDF, presentations, spreadsheets, emails, databases, eBooks, and many others.

### Download or Configure

You may download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/parser), or just get the latest repository and dependency configurations for the pox.xml of your **maven-based** Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>https://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
	<groupId>com.groupdocs</groupId>
	<artifactId>groupdocs-parser</artifactId>
	<version>21.2</version> 
</dependency>
```

## How to Extract ZIP Files Data in Java {#how-to-extract-zip-data}

To extract the data from any file that is enclosed within the archive, you first need to get all the enclosed files. After that, you can further extract any kind of data from each file. The following steps show how to extract ZIP files data and retrieve text from each enclosed file in Java.

*   Load the ZIP archive using **[Parser](https://apireference.groupdocs.com/parser/java/com.groupdocs.parser/Parser)** class.
*   Extract the collection of attachments using the **_[getContainer](https://apireference.groupdocs.com/parser/java/com.groupdocs.parser/Parser#getContainer())_** method.
*   Traverse the attachments for the data of each enclosed file.
*   You can get its different kind of data using respective methods of the **Parser** class.

The source code shows how to extract the ZIP files data using Java. The example below extracts the whole text from all the files within the ZIP archive.

{{< gist GroupDocsGists 6ac7a940cd05a19520d18e7648756c6f "ExtractDataFromZipArchive.java" >}}

The output of the above source code shows the retrieved text of one of the PDF files within the ZIP file.

```
 -----------------------------------
 Name: sample.pdf
 File Size: 33370 Bytes
 -----------------------------------

 Heading

 This is the first paragraph of the sample document that contains some sample
 text, bulleted list, numbered list and more.

    •  Bullet Item 1
    •  Bullet Item 2
    •  Bullet Item 3
 
 This is the second paragraph of the sample document and after this, there is a
 numbered list: 

    1. Numbered Item 1
    2. Numbered Item 2
    3. Numbered Item 3 
```

## Extract Images from Files within ZIP files in Java {#extract-images-from-zip-data}

Not limited to just text, you can also similarly extract the images information. The following steps show how to extract ZIP files data and retrieve images information from each enclosed file.

*   Load the ZIP archive using **[Parser](https://apireference.groupdocs.com/parser/java/com.groupdocs.parser/Parser)** class.
*   Extract the collection of attachments using the **_[getContainer](https://apireference.groupdocs.com/parser/java/com.groupdocs.parser/Parser#getContainer())_** method.
*   Traverse the attachments to get the collection of images within each attachment.
*   Now traverse the images to get the information of each image using  **[PageImageArea](https://apireference.groupdocs.com/parser/java/com.groupdocs.parser.data/PageImageArea)** class.

The following source code shows how to extract images data from the files enclosed within the ZIP files in Java.

{{< gist GroupDocsGists 6ac7a940cd05a19520d18e7648756c6f "ImagesDataFromFilesWithinZipArchive.java" >}}```
Image# 1 
Page: 1
File Type: JPEG Image (.jpeg) 
```

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

In short, you have learned how to extract ZIP archives data within your Java applications. Additionally, you can also extract images from the ZIP files using GroupDocs.Parser for Java. Start building your data extraction Java application for compressed files. To learn more about the API, visit the [documentation](https://docs.groupdocs.com/parser/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Extract ZIP Files Data in C#](https://blog.groupdocs.com/2021/08/25/extract-zip-files-data-in-csharp/)
*   [Get Images from Documents using Java](https://blog.groupdocs.com/2020/10/27/extract-images-from-pdf-word-excel-ppt-using-java/)
*   [Extract Images from EPUB, FB2, CHM eBooks in Java](https://blog.groupdocs.com/2021/03/15/extract-images-from-ebooks-in-java/)




