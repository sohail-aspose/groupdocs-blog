---
title: 'Password Protection of PDF Files in Java'
date: Tue, 07 Dec 2021 07:36:00 +0000
draft: false
url: /2021/12/07/password-protect-pdf-files-in-java/
author: 'Shoaib Khan'
summary: 'There are different security levels that you can provide to your confidential documents. You can apply watermarks, encrypt files, or you can make your documents password-protected. In this article, we will see **how to programmatically add password protection to the PDF files within the Java applications**. Further, we will learn to **change the password** and also to **remove the passwords** to unlock PDF files.'
tags: ['Add Password to PDF in Java', 'Change PDF Password in Java', 'Lock PDF in Java', 'Password Protect Document', 'Remove Password in Java', 'Unlock PDF in Java']
categories: ['GroupDocs.Merger Product Family']
---

There are different security levels that you can provide to your confidential documents. You can [apply watermarks](https://blog.groupdocs.com/category/watermark/), encrypt files, or you can [make your documents password-protected](https://blog.groupdocs.com/?s=password). In this article, we will see **how to programmatically add password protection to the PDF files within the Java applications**. Further, we will learn to **change the password** and also to **remove the passwords** to unlock PDF files.



{{< figure align=center src="images/password-protect-lock-unlock-pdf-in-java.jpg" alt="Protect PDF Files with Password in Java - Lock Unlock">}}


The following topics are discussed below:

*   [Java API for Password Protection of PDF Files](#lock-unlock-pdf-java-api)
*   [Password Protect PDF Files in Java](#lock-pdf-by-password)
*   [Change PDF Password in Java](#change-pdf-password)
*   [How to Remove PDF Password - Unlock PDF](#remove-password-to-unlock-pdf)

## Java API to Lock and Unlock PDF Files {#lock-unlock-pdf-java-api}

[GroupDocs.Merger for Java](https://products.groupdocs.com/merger/java/) is the API that allows to lock and unlock documents. We will use it to add, change, and remove password security features for the PDF documents within the Java applications. Along with protecting and unprotecting documents, the API provides many more features like splitting, merging documents, and many more that are mentioned in the [documentation](https://docs.groupdocs.com/merger/java/).

You can download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/merger) or use the latest repository and dependency [Maven](https://repository.groupdocs.com/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs) configurations within your Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-merger</artifactId>
        <version>21.9</version> 
</dependency>
```

## Add Password to PDF in Java - Lock PDF {#lock-pdf-by-password}



{{< figure align=center src="images/locked-PDF.jpg" alt="Lock PDF with Password">}}


Let's quickly jump to add password protection to the PDF files for security. The following steps show how to add a password to PDF documents in Java.

*   Define the password using [AddPasswordOptions](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/AddPasswordOptions) class.
*   Load the PDF file using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class.
*   Protect the file by adding password using [addPassword()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#addPassword(com.groupdocs.merger.domain.options.interfaces.IAddPasswordOptions)) method.
*   Save the protected file using the [save()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

The following code snippet adds a password to a PDF file in Java.

{{< gist GroupDocsGists 4be8e5153e84bf9c2d55f74f11f07543 "AddPasswordToPDF.java" >}}

If you try to open the password-protected PDF file, the PDF viewer will ask to enter the password.



{{< figure align=center src="images/enter-pwd-to-protected-pdf-1024x298.png" alt="Enter Password to Protected PDF">}}


## Update Existing Password of PDF Files in Java {#change-pdf-password}

What if your secret is no more a secret? Make it secret again. Let's change the password to a new one. The following steps change the existing password of a PDF file in Java.

*   Set the [loading options](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/LoadOptions) using the current password.
*   Now set the [update options](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/UpdatePasswordOptions) using the new password.
*   Load the PDF document using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class and the loading options.
*   Change the existing password using [updatePassword()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#updatePassword(com.groupdocs.merger.domain.options.interfaces.IUpdatePasswordOptions)) method.
*   Save the password protected file again with the updated password using the [save()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

The code snippet changes the current password of the PDF document using Java code.

{{< gist GroupDocsGists 4be8e5153e84bf9c2d55f74f11f07543 "ChangePdfPassword.java" >}}

## Remove Password from PDF Files in Java - Unlock PDF {#remove-password-to-unlock-pdf}



{{< figure align=center src="images/unlocked-PDF.jpg" alt="PDF unlocked - Removed Password">}}


If file protection is not more needed, you can remove the password. The following steps show how to remove the password of a protected PDF file in Java.

*   Prepare the [load options](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger.domain.options/LoadOptions) using the existing password.
*   Load the PDF document using [Merger](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger) class using load options.
*   Remove its password using [removePassword()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#removePassword()) method.
*   Save the unlocked file using the [save()](https://apireference.groupdocs.com/merger/java/com.groupdocs.merger/Merger#save(java.lang.String)) method.

The following is the Java code example to remove the password of a PDF file to make it unlocked.

{{< gist GroupDocsGists 4be8e5153e84bf9c2d55f74f11f07543 "RemovePdfPassword.java" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## Conclusion

To conclude, we discussed the password protection of PDF documents. Initially, we locked the PDF file by adding a password. Then, we changed its password. Lastly, we removed the PDF file password to keep these unlocked. Now you can think about building your own password protector & password remover Java application.

To learn more about GroupDocs.Merger for Java, visit the [documentation](https://docs.groupdocs.com/merger). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Ways to Split PDF Files in Java](https://blog.groupdocs.com/2021/10/19/split-pdf-files-in-java/)
*   [Watermark PDF Files in Java](https://blog.groupdocs.com/2021/06/26/add-watermark-to-pdf-in-java/)
*   [Password Protection for PDF files using C#](https://blog.groupdocs.com/2021/11/17/lock-unlock-pdf-files-with-password-using-csharp/)




