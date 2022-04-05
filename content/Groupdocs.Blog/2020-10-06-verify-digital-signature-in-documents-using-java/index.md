---
title: 'Verify Digital Signature in Documents using Java'
date: Tue, 06 Oct 2020 11:24:19 +0000
draft: false
url: /2020/10/06/verify-digital-signature-in-documents-using-java/
author: 'Shoaib Khan'
summary: 'In this article, we will be learning to **programmatically verify the digitally signed documents using Java**. The example uses PDF document for the verification, however, you may also perform verification of digitally signed word processing documents like MS Word **DOC/DOCX**, Excel spreadsheets **XLS/XLSX**, and presentations **PPT/PPTX**.'
tags: ['verify digital signatures in java', 'verify digitally signed documents in java']
categories: ['GroupDocs.Signature Product Family']
---

Certificate-based digital signatures are the type of electronic signature that provides the highest level of assurance of a signer's identity and complies with strict regulations. In this article, we will be learning to **programmatically verify the digitally signed documents using Java**. In one of the [earlier posts](https://blog.groupdocs.com/2019/09/25/verify-digital-signature-in-documents-using-csharp/), we have discussed the verification of digital signatures in documents using C#.

## Java API for Signature Verification



{{< figure align=center src="images/groupdocs-signature-java.png" alt="GroupDocs.Signature for Signing Documents using Java">}}


This article uses Document Signature API for Java by GroupDocs. The [GroupDocs.Signatures for Java](https://products.groupdocs.com/signature/java) supports the following types of electronic signatures:

*   Barcode Signatures
*   Form-Field Signatures
*   Image Signatures
*   Metadata Signatures
*   QR-Code Signatures
*   Stamp Signatures
*   Text Signatures

So, it is better to prepare your workspace beforehand either by downloading the library from the [downloads section](https://downloads.groupdocs.com/signature/java) or by setting the mentioned configuration in your Maven-based applications.

## Steps to Verify Digitally Signed PDF Document using Java

By following the steps, you can verify the digitally signed documents. In this example, I have used a **PDF** document for verification, however, the same steps will work for **MS Word** documents, **Excel** spreadsheets, and **Powerpoint** presentations.

1.  Instantiate the [Signature](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature/Signature) object with the source document.
2.  Instantiate the [DigitalVerifyOptions](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature.options.verify/DigitalVerifyOptions) class object and specify verification options.
3.  Call [verify](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature/Signature#verify(com.groupdocs.signature.options.verify.VerifyOptions)) method of Signature and pass the specified verification options.

Below is the full sample source code that shows the above process. Here the Java code verifies the digitally signed PDF document. You may also perform verification of digitally signed word processing documents like MS Word **DOC/DOCX**, Excel spreadsheets **XLS/XLSX**, and presentations **PPT/PPTX**.

{{< gist GroupDocsGists 860444814f9530f71f311781b9f5e606 "VerifyDigitalSignature.java" >}}

## Conclusion

Today, we learned to verify the digitally signed MS Word, Excel, PowerPoint, and PDF documents using Java. You can explore more about **GroupDocs.Signature for Java** features using the [documentation articles](https://docs.groupdocs.com/signature/java).

## See Also

*   [Verify Digital Signatures in Documents using C#](https://blog.groupdocs.com/2019/09/25/verify-digital-signature-in-documents-using-csharp/)




