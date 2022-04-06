---
title: "'使用 Java 搜索和替换 Word 文档中的文本'"
date: Fri, 04 Feb 2022 15:24:00 +0000
draft: false
url: /zh/2022/02/04/find-and-replace-text-in-word-documents-using-java/
author: 'Shoaib Khan'
summary: "在其中一篇文章中，我们已经讨论了[如何以 .NET 开发人员的身份编辑文档中的单词](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in-文件-使用-csharp/)。该策略以多种方式用于擦除敏感内容、隐藏或删除电子邮件地址或身份证号等私人信息。本文讨论了**如何在 Java 中执行 Word DOC/DOCX 文档中的单词搜索。** 我们将分别讨论如何使用 Java API 进行编校，使用不同的技术来**查找和替换文本、单词或短语**。"
tags: ['how to redact in word', 'how to redact PDF in Java', 'how to redact Word in Java', 'Java Redaction API', 'Redact in Java']
categories: ['GroupDocs.Redaction Product Family']
---

在其中一篇文章中，我们已经讨论了[如何以 .NET 开发人员的身份编辑文档中的单词](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in-文件-使用-csharp/)。该策略以多种方式用于擦除敏感内容、隐藏或删除电子邮件地址或身份证号等私人信息。本文讨论**如何使用 Java 在 Word DOC/DOCX 文档中执行单词搜索。** 我们将分别讨论如何使用 Java API 进行编校，以不同的技术**查找和替换文本、单词或短语**。

下面将介绍以下主题：

* [用于单词搜索和替换文本的 Java API](#word-search-java-api)
* [查找和替换单词或短语](#replace-word-or-phrase)
* [区分大小写的单词搜索和替换文本](#case-sensitive-text-redaction)
* [使用正则表达式替换文本 (RegEx)](#replace-text-using-regex)
* [用彩色框替换文本](#hide-text-with-colored-box)

## 用于单词搜索和替换文本的 Java API {#word-search-java-api}

**GroupDocs** 提供 [Java 编校 API](https://products.groupdocs.com/redaction/java/)，允许查找和替换 MS Word 支持的文件和其他各种文件格式的其他文档的内容。除了文本编辑和光栅化之外，API 还支持元数据、注释、电子表格以及图像编辑功能。文档中提供了 Word 文档、电子表格、演示文稿、图像和 PDF 文档的[支持的文件格式](https://docs.groupdocs.com/redaction/java/supported-document-formats/)。

### 下载或配置

您可以从 [下载部分](https://downloads.groupdocs.com/redaction) 下载 **JAR** 文件，或者只获取 **maven- 的 pox.xml 的最新存储库和依赖项配置基于** Java 应用程序。

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>https://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
<groupId>com.groupdocs</groupId>
<artifactId>groupdocs-redaction</artifactId>
<version>21.12</version>
</dependency>
```

MS Word or any other third-party software is not required for the redaction process. Let’s now start with different approaches to deal with search and replace text. The following is the screenshot of a Word document that is used in the below examples. You can use the same methods for other document formats as well with very little or no change in the source code.



{{< figure align=center src="images/original-doc.png" alt="Document to redact text">}}


## Find and Replace Words or Phrase using Java {#replace-word-or-phrase}

The following steps explain how to find and then replace the occurrences of a word/phrase in a Word document within the Java application.

*   Load the DOC/DOCX file using [Redactor](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction/Redactor) class.
*   Find the exact phrase or word, using the [ExactPhraseRedaction](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/ExactPhraseRedaction) and [ReplacementOptions](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/ReplacementOptions) classes.
*   Use apply method of Redactor to apply redaction.
*   To save the file at different location after making changes, use the output stream.
*   Save the redaction changes using the [save](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction/Redactor#save(java.io.OutputStream,%20com.groupdocs.redaction.options.RasterizationOptions)) method.

The following code finds and replaces the word "John Doe" in the above Word document using Java. It replaces all the occurrences of “John Doe” with the word “\[censored\]”.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "ReplaceExactPhrase.java" >}}

The output of the code is as follows.



{{< figure align=center src="images/Exact-Phrase-Replacement.png" alt="Redact using Exact Phrase">}}


## Case-Sensitive Word Search and Replace Text in Java {#case-sensitive-text-redaction}

You seem cautious about the exact letter case of the word and only want to replace the word that only matches your case-sensitive search. The following code replaces the existence of the exact case match of the word “John Doe” in Java.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "ReplaceExactPhraseCaseSensitive.java" >}}

The output of the code is as follows.



{{< figure align=center src="images/Case-Sensitive-Exact-Phrase-Redaction.png" alt="Case sensitive redaction">}}


## Replace Text using Regular Expressions (RegEx) in Java {#replace-text-using-regex}

If you do not want to change the exact word but some pattern that exists in your document, you can use the Regular expressions. The following steps allow you to find and replace any pattern of text using regular expressions (RegEx) within your Java applications.

*   Load the document using [Redactor](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction/Redactor) class.
*   Create the RegEx using the [RegexRedaction](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/RegexRedaction).
*   Provide the text using [ReplacementOptions](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/ReplacementOptions) to replace the RegEx match.
*   Use apply method replace all the regex matches.
*   Use the save method to get the redacted document.

The following code shows how to perform the word search in a Word file using RegEx and replace it with some other text using Java.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "ReplaceTextWithRegEx.java" >}}

The following is the output of the above code:



{{< figure align=center src="images/Regex-Redaction.png" alt="RegEx Redaction">}}


## Replace the Text with Colored Box in Java {#hide-text-with-colored-box}

If you do not want to replace your content and just want to hide it, the API allows you to cover to text match by drawing a box over it. The following Java code hides the text with the black rectangle box.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "FindTextAndHide.java" >}}

The output of the above code is as follows.



{{< figure align=center src="images/Colored-Box-Redaction.png" alt="Hide Text using Box">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, you learned how to perform word search to find text in Word documents using exact text phrase search, case-sensitive search, search using regular expressions, and last but not least hiding the text instead of replacing it. You can use these different techniques to replace the findings in different ways within MS Word documents.

For more details and learning about the API, visit the [documentation](https://docs.groupdocs.com/redaction). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Build Full-Text Search Solution in Java](https://blog.groupdocs.com/2021/08/07/build-full-text-search-solution-in-java/)
*   [Image Comparison in Java to Spot the Differences](https://blog.groupdocs.com/2021/06/16/compare-images-in-java/)
*   [Rearrange Pages in Word using Java](https://blog.groupdocs.com/2022/03/01/move-word-pages-using-java/)
*   [Find and Replace Text in PDF using C#](https://blog.groupdocs.com/2022/02/19/find-and-replace-text-in-pdf-using-csharp/)





