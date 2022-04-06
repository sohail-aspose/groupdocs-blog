---
title: 'Generate Barcode in Java – Add Barcode to Documents and Images'
date: Wed, 11 Aug 2021 17:05:00 +0000
draft: false
url: /2021/08/11/generate-barcode-in-java-to-sign-documents-and-images/
author: 'Shoaib Khan'
summary: 'Barcoding is one of the ways to present the data in a machine-readable format. Barcodes are normally used as the identification for a large number of items. In this article, you will learn **how to generate barcodes in Java**. Further, you will see, how the generated barcodes can be applied to any of your **documents as well as images** using Java Signature API within your applications.'
tags: ['Add Barcode in Java', 'Apply Barcode to Images in Java', 'eSigning with Java', 'Generate Barcode in Java', 'Sign Documents in Java', 'Sign Documents with Barcode in Java', 'Sign Images with Barcode in Java']
categories: ['GroupDocs.Signature Product Family']
---

Barcoding is one of the ways to present the data in a machine-readable format. Barcodes are normally used as the identification for a large number of items. In this article, you will learn **how to generate barcodes in Java**. Further, you will see, how the generated barcodes can be applied to any of your **documents as well as images** using Java Signature API within your applications.

The following topics are covered below:

*   [Barcode Generator API for Java](#barcode-generator-java-api)
*   [Apply Barcode to documents in Java](#apply-barcode-to-documents)
*   [Apply Barcode to images in Java](#apply-barcode-to-images)

## Java API for Generating Barcodes {#barcode-generator-java-api}

[GroupDocs.Signature](https://products.groupdocs.com/signature/) showcases Java API that allows signing documents, images, or files of different file formats. Using this API, you can easily generate and apply different types of signatures like barcodes, QR Codes, text, image, metadata, digital signatures, stamps, form field signatures, and more. The API also allows customizing the signature in many ways.

### Download or Configure

You may download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/signature), or just get the latest repository and dependency configurations for the pox.xml of your **maven-based** Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-signature</artifactId>
        <version>21.5</version> 
</dependency>
```

## Generate Barcode in Java for Documents and Images {#generate-barcode-in-java}

Barcodes can be programmatically generated with the customized text, appearance, and different encoding types. Some of the supported barcode types include Code 32, Code 128, DotCode, GS1, ISBN, PDF417, Postnet, UPCA, and many more. These barcodes can be applied to a large list of [supported document and image formats](https://docs.groupdocs.com/signature/java/supported-document-formats/).

The following are the main steps to apply barcodes to any document or image.

*   Load the document or image.
*   Generate the barcode along with text, appearance, encoding and other properties.
*   Attach the generated barcode to the selected file.



{{< figure align=center src="images/generate-barcode-using-java-1024x768.png" alt="Generate Barcode in Java">}}


## Generate Barcode & Apply to Documents in Java {#apply-barcode-to-documents}

Generating barcodes and customizing them according to the need is not a complex procedure. Whether the target documents are an MS Word document, PDF file, Excel spreadsheet, or presentation, the steps to add barcode would be the same for all the different formats. The following steps guide how to generate barcodes and apply/attach these to any document in Java.

*   Load the document (PDF, Word document, spreadsheet, PPT, …) using [Signature](https://apireference.groupdocs.com/java/signature/com.groupdocs.signature/Signature) class.
*   Define barcode options using [BarcodeSignOptions](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature.options.sign/BarcodeSignOptions) class.
*   Set barcode properties like encoding type, position, size, background or fore color, font etc.
*   Call the [sign](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature/Signature#sign(java.io.OutputStream,%20com.groupdocs.signature.options.sign.SignOptions)) method to attach the generated barcode with the loaded document.

The following source code generates a barcode and attaches it to a PDF document using Java.

{{< gist GroupDocsGists 3f07e4f0b5facbd3ff0c50efab29d840 "GenerateAndApplyBarcode.java" >}}

## Generate Barcode & Apply to Images in Java {#apply-barcode-to-images}

In a very similar manner, you can apply barcodes to images. Whether you have a JPG, PNG, WebP image, or any other image format like GIF, TIF, CDR, SVG, or any other, you can attach the barcode to the loaded image.

The following are the step to generate barcodes and apply these to any image using Java API.

*   Load your image (JPG, PNG, WebP, …) using [Signature](https://apireference.groupdocs.com/java/signature/com.groupdocs.signature/Signature).
*   Prepare the barcode options using [BarcodeSignOptions](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature.options.sign/BarcodeSignOptions).
*   Customize the barcode by setting text, encoding type, position, size, appearance, etc.
*   Apply barcode to sign the image using [sign](https://apireference.groupdocs.com/signature/java/com.groupdocs.signature/Signature#sign(java.io.OutputStream,%20com.groupdocs.signature.options.sign.SignOptions)) method.

The following source code generates a barcode and attaches it to a JPG image in Java.

{{< gist GroupDocsGists 3f07e4f0b5facbd3ff0c50efab29d840 "GenerateAndApplyBarcodeToImages.java" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you have learned how to generate the barcodes in Java. Further, you have seen how to add these generated barcodes to your images and documents. Now you can develop your own barcode generator Java application.

You can learn more about the Java Signature API using the [documentation](https://docs.groupdocs.com/signature/java/) or by examples available on [GitHub](https://github.com/groupdocs-signature). Get in touch with us at the [forum](https://forum.groupdocs.com/).

## See Also

*   [Generate QR Codes for images and documents in Java](https://blog.groupdocs.com/2021/02/19/generate-qr-codes-in-java-to-sign-documents-and-images/)
*   [Generate QR Codes in C# for documents and images](https://blog.groupdocs.com/2021/01/27/generate-qr-codes-in-csharp-to-sign-documents-and-images/)




