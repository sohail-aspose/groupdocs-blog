---
title: 'Metadata Remover for Documents and Images using  C#'
date: Tue, 29 Dec 2020 14:14:00 +0000
draft: false
url: /2020/12/29/remove-metadata-of-documents-and-images-using-csharp/
author: 'Shoaib Khan'
summary: 'Today we are about to learn some ways to **programmatically remove or entirely clean metadata of documents as well as images using C#**. In an [earlier post](https://blog.groupdocs.com/2020/12/17/remove-metadata-from-documents-and-images-using-java/), we discussed removing the selective as well as all the available metadata properties from documents and images using Java. It is sometimes important to hide personal information from the receiver, that is attached to the document. Following are the topics that will help you clean your files from metadata using C#.

[Continue Reading ...](https://blog.groupdocs.com/2020/12/29/remove-metadata-of-documents-and-images-using-csharp/)'
tags: ['metadata cleaner using csharp', 'remove metadata from documents in csharp', 'remove metadata from images in csharp', 'remove metadata using csharp']
categories: ['GroupDocs.Metadata Product Family']
---

Today we are about to learn some ways to **programmatically remove or entirely clean metadata of documents as well as images using C#**. In an [earlier post](https://blog.groupdocs.com/2020/12/17/remove-metadata-from-documents-and-images-using-java/), we discussed removing the selective as well as all the available metadata properties from documents and images using Java. It is sometimes important to hide personal information from the receiver, that is attached to the document. Following are the topics that will help you clean your files from metadata using C#.

*   [.NET Metadata Cleaner API](#dotnet-metadata-removal-api)
*   [Remove Metadata from Documents using C#](#remove-documents-metadata-using-csharp)
*   [Clean Metadata from Images using C#](#remove-images-metadata-using-csharp)
*   [Remove Selective Metadata from Documents and Images using C#](#remove-selective-metadata-using-csharp)

## .NET Metadata Removing API {#dotnet-metadata-removal-api}

To achieve what is planned, I will use [GroupDocs.Metadata for .NET](https://products.groupdocs.com/metadata/net) API that allows .NET developers to add, modify, extract, remove, or completely metadata from many [supported formats](https://docs.groupdocs.com/metadata/net/supported-document-formats/) of documents, images, and other files. The API supports metadata standards like EXIF, XMP, IPTC, ID3 tag, etc. You may [download](https://downloads.groupdocs.com/metadata/net) DLLs or MSI installer, or install it via [NuGet](https://www.nuget.org/packages/groupdocs.metadata).

```
Install-Package GroupDocs.Metadata
```

## Remove Metadata from Documents using C# {#remove-documents-metadata-using-csharp}

In order to remove all the metadata properties without applying any specific filter, use the **Sanitize** method. The following are the steps to clean metadata from the documents like DOCX, PDF, XLSX, etc using GroupDocs.Metadata for .NET.

*   Start by creating [Metadata](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata) class object and pass the path of the target document as the parameter.
*   Use [Sanitize](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata/methods/sanitize) method to clear all the available metadata. It returns the number of the removed metadata properties.
*   Call [Save](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata/methods/save/index) method to save the output file with removed metadata.

The following C# code sample shows how to remove and clear metadata from a PDF document.

{{< gist GroupDocsGists 9aa3d162544a32eeff377b6caa6fdf4a "DocumentMetadataCleaner.cs" >}}

## Remove Metadata from Images using C# {#remove-images-metadata-using-csharp}

Whether you want to remove metadata from your documents or from your image files, the process will remain the same. Only the source document will be changed accordingly.

*   Create the object of the [Metadata](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata) class and pass the document path as the parameter.
*   Call the [Sanitize](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata/methods/sanitize) method to remove any available metadata properties.
*   Save the output file using the [Save](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata/methods/save/index) method.

The following C# code sample shows how to remove metadata from a JPG image.

{{< gist GroupDocsGists 9aa3d162544a32eeff377b6caa6fdf4a "ImageMetadataCleaner.cs" >}}

## Remove Selective Metadata from Documents and Images using C# {#remove-selective-metadata-using-csharp}

If it is not required to remove all the available metadata from the files, and we just want to remove only the selective metadata properties. The following steps allow you to locate and remove the targetted metadata properties using the specific name of the property.

*   Create an object of [Metadata](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata) class to load the source document or image file.
*   Create personalized specifications to find the metadata properties.
*   Call the [RemoveProperties](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata/methods/removeproperties) method with the created personalized specifications.
*   Save the output file using the [Save](https://apireference.groupdocs.com/metadata/net/groupdocs.metadata/metadata/methods/save/index) method.

{{< gist GroupDocsGists 6114128ca015cbb1740cd8e05fd62fb3 "RemoveSpecificMetadataProperties.cs" >}}

## Conclusion

We learned the ways to remove metadata from documents and images using C#. After going through this article, you would feel comfortable building your own metadata cleaner application using .NET. It can support metadata removal from MS Word document formats, spreadsheets, presentations, PDF files, images, emails, eBooks, drawings, zip files, and many more [file formats that are supported by the API](https://docs.groupdocs.com/metadata/net/supported-document-formats/).

You may further explore the [.NET Metadata Manipulation API](https://products.groupdocs.com/metadata/net) from the [documentation](https://docs.groupdocs.com/metadata/net/).

## See Also

*   [Remove Metadata of Documents and Images in Java](https://blog.groupdocs.com/2020/12/17/remove-metadata-from-documents-and-images-using-java/)
*   [Manage EXIF Data of Images in C#](https://blog.groupdocs.com/2020/05/13/manage-exif-data-in-csharp-net-for-jpeg-png-tiff-webp-images/)
*   [Manage EXIF Data of Images using Java](https://blog.groupdocs.com/2020/05/12/handle-exif-data-of-jpg-png-webp-images-in-java/)




