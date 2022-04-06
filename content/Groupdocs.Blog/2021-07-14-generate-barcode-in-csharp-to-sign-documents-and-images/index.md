---
title: 'Generate Barcode in C# - Add Barcode to Documents and Images'
date: Wed, 14 Jul 2021 17:25:00 +0000
draft: false
url: /2021/07/14/generate-barcode-in-csharp-to-sign-documents-and-images/
author: 'Shoaib Khan'
summary: 'Barcode is way to present the data in machine readable format. Barcodes are normally used for quick identification of large number of items. In this article, you will learn how to generate barcodes within .NET applications. Futher you will see, how the generated barcodes can be applied to any of your documents and images using C#.'
tags: ['Apply Barcode to Images in C#', 'Apply Barcode to PDF in C#', 'Generate Barcode in C#', 'Sign Documents with Barcode in C#', 'Sign Images with Barcode in C#']
categories: ['GroupDocs.Signature Product Family']
---

Barcode is a way to present the data in a machine-readable format. Barcodes are normally used for the quick identification of a large number of items. In this article, you will learn how to generate barcodes within .NET applications. Further, you will see, how the generated barcodes can be applied to any of your documents and images using C#.

The following topics are covered below:

*   [Barcode Generator API for .NET](#barcode-generator-dotnet-api)
*   [Generate & apply barcode to documents in C#](#apply-barcode-to-documents)
*   [Generate & apply barcode to images in C#](#apply-barcode-to-images)

## .NET API for Generating Barcodes {#barcode-generator-dotnet-api}

[GroupDocs.Signature](https://products.groupdocs.com/signature/) has the .NET API that allows you to sign your documents, images, or files of different file formats. Using this API, you can easily apply different types of signatures like QR Codes, barcodes, text, image, metadata, digital signatures, stamps, electronic signatures. Further, you can customize the appearance of the signature in many ways.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/signature) or install the API for your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.signature). You may also use the following command from the Package Manager.

```
PM> Install-Package GroupDocs.Signature
```

## Barcodes for Documents and Images using C# {#generate-barcode-in-csharp}

Barcodes can be programmatically generated with the customized text, appearance, and different encoding types. Some of the supported barcode types include Code 32, Code 128, DotCode, GS1, ISBN, PDF417, Pharmacode, Postnet, UPCA, and many more. These barcodes can be applied to a large list of [supported document and image formats](https://docs.groupdocs.com/signature/net/supported-document-formats/).

The following are the main step to apply barcodes on any document or image.

*   Load the document or image.
*   Generate the barcode along with text, appearance, encoding and other properties.
*   Apply it on the loaded file.



{{< figure align=center src="images/Generate-Barcode-using-GroupDocs.jpg" alt="Generate Barcode in C#">}}


## Generate Barcode & Apply to Documents in C# {#apply-barcode-to-documents}

The following are the step to generate barcodes and apply these to any document. Whether the target documents are an MS Word document, PDF file, Excel Spreadsheet, or Presentation, the steps to add barcode would be the same for all the different formats.

*   Load the document (PDF, Word Doc, Spreadsheet, PPT, ...) using [Signature](https://apireference.groupdocs.com/signature/net/groupdocs.signature/signature) class.
*   Setup barcode options using [BarcodeSignOptions](https://apireference.groupdocs.com/signature/net/groupdocs.signature.options/barcodesignoptions) class.
*   Set barcode properties like encoding type, position, size, etc.
*   Call the [Sign](https://apireference.groupdocs.com/signature/net/groupdocs.signature/signature/methods/sign) method to apply barcode and sign the loaded document.

The following source code generates a barcode and attaches it to a PDF document using C#.

{{< gist GroupDocsGists bceca465883f710a35bf6c447f251634 "GenerateAndApplyBarcode.cs" >}}

## Generate Barcode & Apply to Images in C# {#apply-barcode-to-images}

Similarly, the way to apply barcodes on images is not different. Just load the right image, the rest of the steps and code will remain the same as used for applying barcodes to the documents above.

The following are the step to generate barcodes and apply these to any image.

*   Load the image (JPG, PNG, WebP, ...) using [Signature](https://apireference.groupdocs.com/signature/net/groupdocs.signature/signature).
*   Prepare barcode options using [BarcodeSignOptions](https://apireference.groupdocs.com/signature/net/groupdocs.signature.options/barcodesignoptions).
*   Customize the barcode by setting text, encoding type, position, size, appearance, etc.
*   Apply barcode to sign the image using [Sign](https://apireference.groupdocs.com/signature/net/groupdocs.signature/signature/methods/sign) method.

The following source code generates a barcode and attaches it to a JPG image using C#.

{{< gist GroupDocsGists bceca465883f710a35bf6c447f251634 "GenerateAndApplyBarcodeToImages.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, you learned how to generate the barcode in C#. Further, you have seen how to add these generated barcodes to your images and documents. Now you can develop your own barcode generator .NET application.

You can learn more about the .NET Signature API using the [documentation](https://docs.groupdocs.com/signature/net/), or by examples available on [GitHub](https://github.com/groupdocs-signature). Get in touch with us at the [forum](https://forum.groupdocs.com/).

## See Also

*   [Generate QR Codes in C# and apply to documents and images as signature](https://blog.groupdocs.com/2021/01/27/generate-qr-codes-in-csharp-to-sign-documents-and-images/)
*   [Generate and apply QR Codes on images and documents in Java](https://blog.groupdocs.com/2021/02/19/generate-qr-codes-in-java-to-sign-documents-and-images/)




