---
title: 'Generate QR Code in C# to Sign Documents and Images'
date: Wed, 27 Jan 2021 22:39:00 +0000
draft: false
url: /2021/01/27/generate-qr-codes-in-csharp-to-sign-documents-and-images/
author: 'Shoaib Khan'
summary: 'In this article, we will see **how to programmatically add QR codes to electronically sign documents and images using C#**. GroupDocs.Signature for .NET is the API to add QR codes in PDF files, word processing documents, spreadsheets, presentations, and images.'
tags: ['Add QR code in CSharp', 'Attach QR code with Images in CSharp', 'eSign in CSharp', 'generate qr code in csharp', 'Sign documents with QR code in CSharp']
categories: ['GroupDocs.Signature Product Family']
---

QR Codes have gained popularity in recent years. As a developer, let us see **how to programmatically generate QR codes in C#** to electronically sign documents and images. In the earlier post, we discussed [attaching QR codes with documents and images using Java](https://blog.groupdocs.com/2021/02/19/generate-qr-codes-in-java-to-sign-documents-and-images/).



{{< figure align=center src="images/add-qr-code-to-docs-and-images-using-dotnet.png" alt="Generate QR Codes in C# .NET to sign documents and images using GroupDocs.">}}


The following topics will be converted in this article:

*   [.NET API for Generating QR codes and Signing](#dotnet-api-for-qr-codes)
*   [Generate QR codes - Sign documents in C#](#add-qr-code-to-documents-in-csharp)
*   [Generate QR codes - Add to JPG, PNG, or WebP image in C#](#add-qr-code-to-images-in-csharp)

## .NET API for QR Codes Generation {#dotnet-api-for-qr-codes}



{{< figure align=center src="images/groupdocs-signature-net-90x90-no-border.png" alt="GroupDocs.Signature for .NET">}}


In this article, I will be using [GroupDocs.Signature for .NET](https://products.groupdocs.com/signature/net) API for generating QR codes. This API supports Aztec Code, DataMatrix Code, GS1 DataMatrix, GS1 QR, QR types. It also supports PDF files, word processing documents, spreadsheets, presentations, images, and a lot more [document file formats to add QR codes](https://docs.groupdocs.com/signature/net/supported-document-formats/).

For the examples below, I would recommend you to either install the API from the [NuGet](https://www.nuget.org/packages/groupdocs.signature) package manager or get the MSI installer, and DLLs from the [downloads](https://downloads.groupdocs.com/signature/net) section. You may also use the following command in your Package Manager Console.

```
PM> Install-Package GroupDocs.Signature
```

For the details, you may visit the [API Reference](https://apireference.groupdocs.com/signature/net).

## Generate QR Codes in C# - Add to PDF, Word, Excel, PPT files {#add-qr-code-to-documents-in-csharp}

The **Signature** and **QrCodeSignOptions** classes help to quickly create different types of QR codes and sign documents and images within .NET application. The following steps show how to generate QR codes using C# and then attach them to a PDF document:

1.  Initialize the **Signature** class object with the source document.
2.  Set the QR code properties using the **QrCodeSignOptions** class.
3.  Most importantly, select the appropriate from the available QR code types. (Aztec, DataMatrix, GS1 DataMatrix, GS1 QR, QR)
4.  Call the **Sign** method, passing the resultant document path and QR code options.

The following C# code implements the above steps. Similarly, you can provide a word document, spreadsheet, presentation, or any other [supported document format](https://docs.groupdocs.com/signature/net/supported-document-formats/) to attach the generated QR codes.

{{< gist GroupDocsGists 4c70c60f1f5bdfce19da18f8b9f6ca11 "SignDocsWithQRCode.cs" >}}

This is the PDF file with QR code as an output of the above code.



{{< figure align=center src="images/Added-QR-Code-in-PDF-using-GroupDocs.Signature-APIs.png" alt="Add generated QR Code to PDF using Signature API" caption="PDF file with added QR code using GroupDocs.Signature for .NET API">}}


## Generate QR Codes in C# - Attach with JPG, PNG, or WebP Images {#add-qr-code-to-images-in-csharp}



{{< figure align=center src="images/image-with-qr-code.png" alt="Add the generated QR code to Image.">}}


You can use the same above code to attach the generated QR codes with the images as well. The API allows you to add QR codes to JPG/JPEG, PNG, WebP, BMP, GIF, SVG, CMX, and TIFF images and some more image file formats as well.

While generating QR codes, you can also change the background color, forecolor, transparency, and some more properties to alter their appearance. The below C#code changes the background color of the QR code to **black** and sets the forecolor to **white**.

{{< gist GroupDocsGists 4c70c60f1f5bdfce19da18f8b9f6ca11 "ChangeQRCodeAppearance.cs" >}}

## Conclusion

I believe, now you are familiar with how to create QR codes in C# to sign your documents and images electronically within .NET applications. You can further change the appearance of the QR codes that suits your brand.

## See Also

*   [Generate QR codes to Sign Documents and Images in Java](https://blog.groupdocs.com/2021/02/19/generate-qr-codes-in-java-to-sign-documents-and-images/)

*   [Documentation](https://docs.groupdocs.com/signature/net/)
*   [Free Support Team](https://forum.groupdocs.com/c/signature)
*   [Examples on GitHub](https://github.com/groupdocs-signature/GroupDocs.Signature-for-.NET)




