---
title: 'Manage XMP and EXIF Data of HEIF/HEIC Images using C#'
date: Sat, 17 Jul 2021 17:58:00 +0000
draft: false
url: /2021/07/17/manage-xmp-and-exif-data-of-heif-heic-images-using-csharp/
author: 'Shoaib Khan'
summary: '**HEIC** (High-Efficiency Image Container) is a container that can contain High-Efficiency Image Format **HEIF** images. **XMP** is an XML-based metadata standard, that can store metadata properties as name/value pairs. However, **EXIF** (Exchangeable Image File Format) is the standard and defines how to store metadata properties in the most common images and audio formats.  In this article, we will learn **how to extract, update, and remove the XMP and EXIP metadata of the HEIF/HEIC images** using C# within .NET applications.

The following topics are covered in this article:

*   .NET API for EXIF, XMP Metadata
*   Read EXIF Data of HEIC/HEIF Images
*   Read XMP data of HEIC/HEIF Images'
tags: ['exif data', 'exif data in CSharp', 'EXIF data of HEIC in CSharp', 'XMP data in CSharp', 'XMP data of HEIC in CSharp', 'XMP metadata']
categories: ['GroupDocs.Metadata Product Family']
---

**HEIC** (High-Efficiency Image Container) is a container that can contain High-Efficiency Image Format **HEIF** images. **XMP** is an XML-based metadata standard, that can store metadata properties as name/value pairs. However, **EXIF** (Exchangeable Image File Format) is the standard and defines how to store metadata properties in the most common images and audio formats.  In this article, we will learn **how to extract, update, and remove the XMP and EXIP metadata of the HEIF/HEIC images** using C# within .NET applications.

The following topics are covered below:

*   [.NET API for EXIF, XMP Metadata](#dotnet-api-for-exif-and-xmp-metadata)
*   [Read EXIF Data of HEIC/HEIF Images](#read-exif-of-heic-heif-images)
*   [Read XMP data of HEIC/HEIF Images](#read-xmp-of-heic-heif-images)

## .NET API for XMP and EXIF Metadata {#dotnet-api-for-exif-and-xmp-metadata}

[GroupDocs.Metadata](https://products.groupdocs.com/metadata) provides .NET API to automate metadata management within .NET applications. The API allows to read, update, add, clean/remove, and traverse the metadata for many file formats. Various metadata standards like EXIF, IPTC, and XMP are supported by the API. You can also visit the documentation for the complete list of [supported file formats for metadata manipulation](https://docs.groupdocs.com/metadata/net/supported-document-formats/).

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/metadata) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.metadata).

```
PM> Install-Package GroupDocs.Metadata
```

## Read EXIF data of HEIC / HEIF Images in C# {#read-exif-of-heic-heif-images}

The following are the steps to read and extract EXIF data of HEIC and HEIF images.

*   Load the HEIF or HEIC image using the Metadata class.
*   Get the root package.
*   Retrieve the EXIF package from the root package.
*   Traverse the EXIF data properties.
*   Furthermore, you can get the IFD (Image File Directory) and GPS information from the EXIF package.

The following code shows how to get EXIF data, IFD and GPS metadata information of the HEIC image using C#.

{{< gist GroupDocsGists 5179cd90a5667444b1a3472a0800fd9a "ReadHeifExif.cs" >}}

## Read XMP data of HEIC / HEIF Images in C# {#read-xmp-of-heic-heif-images}

The following steps reads XMP metadata of HEIC or HEIF images.

*   Load the HEIF or HEIC image using the Metadata class.
*   Get the root package using the getRootPackage method.
*   From the root package, you can get the XMP basic information.
*   Further, you can get the DCMI Dublin Core information.
*   Additionally, you can get Photoshop information using the getPhotoshop method.

The following source code shows how to get XMP basic, DCMI, and Photoshop information in C#.

{{< gist GroupDocsGists 5179cd90a5667444b1a3472a0800fd9a "ReadHeifXmp.cs" >}}

Likewise, there are many setter methods to set or update different XMP properties. You can even [provide your own key-value pair to set the custom XMP package property](https://docs.groupdocs.com/metadata/net/working-with-xmp-metadata/).

## Remove EXIF and XMP Metadata of HEIC/HEIF Images in C#

You can just set the respective EXIF package or XMP package to null to remove all the metadata properties.

The following code removes the EXIF data of HEIC images in C#.

{{< gist GroupDocsGists 5179cd90a5667444b1a3472a0800fd9a "RemoveExifData.cs" >}}

The following code removes the XMP data of HEIC images in C#.

{{< gist GroupDocsGists 5179cd90a5667444b1a3472a0800fd9a "RemoveXmpData.cs" >}}

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, we have learned to extract, update, remove EXIF and XMP metadata from the HEIF/HEIC images in C#. Furthermore, you have seen how to get IFD and GPS information from these images. Now you can easily get this information and also start building your own applications like [GroupDocs.Metadata App Product Family](https://products.groupdocs.app/metadata/family) to automate metadata information.

For more information, options, and examples, you can visit the [documentation](https://docs.groupdocs.com/metadata/) and the [GitHub](https://github.com/groupdocs-metadata) repository. For further queries, contact us on the support [forum](https://forum.groupdocs.com/).

## See Also

*   [Extract RIFF INFO and Metadata of WAV files in C#](https://blog.groupdocs.com/2021/03/05/extract-riff-info-and-metadata-of-wav-files-in-csharp/)
*   [Remove Metadata from Document and Image files using C#](https://blog.groupdocs.com/2020/12/29/remove-metadata-of-documents-and-images-using-csharp/)




