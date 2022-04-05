---
title: 'Edit Word Documents in Java'
date: 
draft: true
url: /?p=23102
author: 'Shoaib Khan'
summary: ''
tags: ['Uncategorized']
---

The most common and widely used word-processing file formats are **DOC**, **DOCX**, and **ODT**. The famous Microsoft Word and OpenOffice Writer support these formats and we normally use these formats for drafting the documents. Therefore, as a developer, we widely need to edit Word documents in our applications programmatically. This article will discuss **how to edit Word documents in Java** using the Java API for document editing.

The following are the topics discussed briefly in this article:

*   Java API for Editing Word Documents
*   Edit Word Documents in Java

## Java API for Word Documents Editing and Automation {#word-editing-dotnet-api}

I will be using GroupDocs.Editor for Java API in examples. It is the document editing API that allows developers to load, edit, and save various document formats using WYSIWYG HTML editors. In addition to the word-processing document formats, the API supports editing spreadsheets, presentations, HTML, XML, TXT, DSV, TSV, and CSV formats.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-editor</artifactId>
        <version>20.11.0</version> 
</dependency>
```

## Edit Word Documents in Java {#edit-word-docs-in-csharp}

Just after setting up the API, you can quickly move towards editing the Word document. The following steps will let you edit the word-processing document.

*   Load the Word document.
*   Edit the document accordingly with options.
*   Save the edited document.

### Load the Word document

Firstly, load the document by providing the document path and the password, if the document is protected.

<code>

### Edit the Word document

After loading, you can edit the loaded document as per your requirement. Here I am replacing all the “document” occurrences with the “edited document” in a Word document using the below Java code.

<code>

### Save the Edited Word document with Options

Lastly, while saving the edited document content, you can further set various options. These options include; pagination, set password, locale, protection, or memory optimization settings. I am setting the above options and saving the edited document as a password-protected and read-only DOCX file in the below-mentioned code.

<code>

### Complete Code

For your convenience, I am showing the complete example that is explained above and it edits the Word document and then saves it in DOCX format in Java.

<code>

The following is the output document in which all the occurrences are replaced using the above code.



{{< figure align=center src="images/edited-document.png" alt="edited docx document using editor API" caption="Output document – All the occurrences are replaced">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

Today, we discussed editing Word documents using document editing Java API. You can use the API with WYSIWYG editors for the visual editing of your documents. After that, you can move ahead to build your own document editor. Similarly, you can also integrate the editing feature within your Java applications.

For more details, options, and examples, you can visit the [documentation](https://docs.groupdocs.com/editor/java) and the [GitHub](https://github.com/groupdocs-editor) repository. For further queries, contact the support on the [forum](https://forum.groupdocs.com/c/assembly).

## See Also

*   [On-Premise Document Editing APIs](https://products.groupdocs.com/editor/family)
*   [Document Editing and Automation Cloud APIs](https://products.groupdocs.cloud/editor/family)
*   [Edit Word Documents Online](https://products.groupdocs.app/editor/word)



