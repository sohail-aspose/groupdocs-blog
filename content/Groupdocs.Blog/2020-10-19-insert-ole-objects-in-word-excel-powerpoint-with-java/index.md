---
title: 'Insert OLE Objects in Word, Excel, PowerPoint using Java'
date: Mon, 19 Oct 2020 06:02:40 +0000
draft: false
url: /2020/10/19/insert-ole-objects-in-word-excel-powerpoint-with-java/
author: 'Shoaib Khan'
summary: 'Today, we will be learning to **embed PDF** and other different documents **as OLE objects in Word, Excel, PowerPoint files using Java**. For embedding the documents via **Object Linking and Embedding**, we will be using the GroupDocs.Merger for Java API that also allows us to efficiently combine/merge and split multiple documents with minimum lines of Java code.

Steps shown here will guide you to:

*   Insert PDF as OLE object into MS Word document.
*   Embed Word document as OLE object into Excel spreadsheet.
*   Insert Excel sheets as OLE object into presentations.'
tags: ['embed OLE objects using Java', 'insert OLE objects in Excel using Java', 'insert OLE objects in java', 'insert OLE objects in presentations using Java', 'insert OLE objects in Word using Java']
categories: ['GroupDocs.Merger Product Family']
---

In one of the earlier posts, we learned how to programmatically [insert the OLE Objects in documents with C#](https://blog.groupdocs.com/2020/05/16/insert-ole-objects-in-word-excel-powerpoint-with-csharp/). Today, in this article, we will be embedding PDF and other different documents as **OLE objects in Word documents, Excel spreadsheets, PowerPoint presentation slides using Java**.

This article will guide you about:

*   [Java API for OLE Objects](#java-api-for-ole-objects)
*   [Insert OLE Objects into MS Word Documents using Java](#insert-ole-object-into-word-in-java)
*   [Add OLE Objects into Excel Spreadsheets using Java](#insert-ole-object-into-excel-in-java)
*   [Insert Documents into Presentations via OLE using Java](#insert-ole-object-into-ppt-in-java)

## Java API for OLE Objects {#java-api-for-ole-objects}



{{< figure align=center src="images/groupdocs-merger-java-90x90-no-reply.png" alt="GroupDocs.Merger for Java">}}


Steps and the examples in this article use [GroupDocs.Merger for Java](https://products.groupdocs.com/merger/java/) to insert documents into other documents via OLE (_Object Linking and Embedding_). This API also allows us to efficiently combine and split multiple documents with minimum lines of Java code. Before proceeding it will be better if you prepare the environment in any of your relevant ways:

1.  **Download** the API from the [downloads](https://downloads.groupdocs.com/merger/java) section.
2.  For the **Maven-based** projects, the following is the configuration for your **pom.xml**

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-merger</artifactId>
        <version>20.7</version> 
</dependency>
```

## Insert PDF as OLE Object into MS Word Document using Java {#insert-ole-object-into-word-in-java}



{{< figure align=center src="images/PDF-in-Word.png" alt="Insert PDF in Word Document">}}


Step and code example below **inserts the PDF document into a Word document as an OLE object in Java** using the GroupDocs.Merger API.

1.  Instantiate the [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) object with the source _word processing document_ path or stream.
2.  Initialize the [OleWordProcessingOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/OleWordProcessingOptions) with the path of the PDF document that will be embedded in the Word document.
3.  Call the [importDocument](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#importDocument(com.groupdocs.merger.domain.options.interfaces.IImportDocumentOptions)) method of the merger class.
4.  Save the resultant word document by calling the [save](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

{{< gist GroupDocsGists 313e9882bedaa1e65c5a540d4f30c8b0 "EmbedDocumentToWordOLE.java" >}}

## Insert Word Document as OLE Object into Excel Spreadsheet using Java {#insert-ole-object-into-excel-in-java}



{{< figure align=center src="images/Word-in-Excel.png" alt="Insert Word File in Excel Spreadsheet">}}


Spreadsheets can also embed other documents, like Word documents, spreadsheets, presentations, images or sound clips, etc. Here, I am be adding a Word document into a spreadsheet as an OLE object.

1.  Initialize the [OleSpreadsheetOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/OleSpreadsheetOptions) class object by providing the path of the Word document that will be embedded in the spreadsheet.
2.  Set the options like row and column positions.
3.  Initialize the [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class object with the path of the spreadsheet document.
4.  Call the [importDocument](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#importDocument(com.groupdocs.merger.domain.options.interfaces.IImportDocumentOptions)) method by providing the already set OLE spreadsheet option.
5.  Save the resultant spreadsheet having the embedded Word document by calling the [save](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

{{< gist GroupDocsGists 3ebe23286748c319a6b5429b1bda9696 "EmbedDocumentToExcelOLE.java" >}}

## Insert Excel Sheet as OLE Object into Presentation using Java {#insert-ole-object-into-ppt-in-java}



{{< figure align=center src="images/Add-Excel-Sheet-in-PPT-Presentation-OLE.png" alt="Insert Excel Sheet in PowerPoint">}}


Similarly, if we need to add any external document(s) to our presentations, these can be inserted at the precise location with the few lines of Java code mentioned-below:

1.  Initialize the [OlePresentationOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/OlePresentationOptions) class object and pass the path of the spreadsheet document.
2.  Set the OLE presentation options like x and y coordinates, height and width for the upcoming embedded spreadsheet.
3.  Instantiate the [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class object with the presentation document path as parameter.
4.  Embed the spreadsheet into presentation using the [importDocument](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#importDocument(com.groupdocs.merger.domain.options.interfaces.IImportDocumentOptions)) method of the Merger class.
5.  Call [save](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method to get the resultant presentation file.

{{< gist GroupDocsGists e3a9ef77464fbb0818d81c79cdf18a06 "EmbedDocumentToPresentationsOLE.java" >}}

## Conclusion

We have learned, **how we can programmatically insert OLE objects in Word, Excel, and Powerpoint documents using Java**. The major difference while embedding the documents into various kinds of source documents is just the use of the respective OLE Options class. That's it.

To learn more about the Merger API for Java, visit [documentation](https://docs.groupdocs.com/merger/java/). In case of any query, GroupDocs Support Team will more than happy to facilitate you at [Free Support Forum](https://forum.groupdocs.com/c/merger).

## See Also

*   [Insert OLE Objects in Word, Excel, PowerPoint using C#](https://blog.groupdocs.com/2020/05/16/insert-ole-objects-in-word-excel-powerpoint-with-csharp/)




