---
title: 'Image Comparison in C# to Spot the Differences'
date: Wed, 06 Jan 2021 17:52:00 +0000
draft: false
url: /2021/01/06/compare-images-in-csharp-dotnet/
author: 'Shoaib Khan'
summary: 'Whether you want to build an application with spot the difference feature or if you want to compare two images within any of your image processing .NET based applications, you are at the right place. After this article, you can easily compare JPG, PNG, BMP, or images with some other file formats. Without wasting time, let us compare images in C# using the [.NET API for document and image conversion](https://products.groupdocs.com/comparison/net).'
tags: ['compare images in csharp', 'compare jpg or png in csharp', 'Image Comparison', 'image comparison in csharp']
categories: ['GroupDocs.Comparison Product Family']
---

Whether you want to build an application with spot the difference feature or if you want to compare two images programmatically within any of your .NET based image processing applications, you are at the right place. After this article, you can easily compare JPG, PNG, BMP, or images with some other file formats. Without wasting time, let's compare images in C# using the [.NET API for document and image comparison](https://products.groupdocs.com/comparison/net).



{{< figure align=center src="images/compare-images-to-find-differences-in-dotnet.jpg" alt="Compare Images for Differences using .NET">}}


## .NET Image Comparison API

I will be using [GroupDocs.Comparison for .NET](https://products.groupdocs.com/comparison/net) API for comparing images in this article. This API supports comparing **JPG, PNG, BMP, DICOM, DCM, DjVu** images along with many other [supported file formats](https://docs.groupdocs.com/comparison/net/supported-document-formats/).

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/comparison/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.comparison).

```
PM> Install-Package GroupDocs.Comparison
```

## Compare Images in C# to Highlight Differences

Comparing two images in C# is too easy with GroupDocs.Comparison within .NET application. The following steps explain how we can compare any two JPG, PNG, BMP, or any other image. It successfully detects the changes and highlights them in the output/resultant image.

*   Define the first image using the [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add the second image using [Add](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/add/index) method of Comparer object.
*   Call [Compare](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method to compare both the images and save the resultant image that highlights the differences among both the images.

The code below shows how to compare two images in C#. As an example, it compares two JPG images and saves the output with differences.

{{< gist GroupDocsGists d1153909e5e54a8c00ccd5ee422a450c "CompareImages.cs" >}}

The images shown at the start of the article are used in this code. Images on the left are compared, and the output is shown on the right side that highlights the differences.

## Conclusion

In this article, we learned how to compare two images in C# using image comparison API. Now you can build your own image comparison application that can compare images and highlight the found differences to its users.

To get a complete idea about the features of the API, you can go through the [documentation](https://docs.groupdocs.com/comparison/net/). You may also contact the [Free Support Team](https://forum.groupdocs.com/c/comparison) or [Free Consulting Team](https://groupdocs-free-consulting.github.io/) that even writes code to help you understand the usage of GroupDocs APIs as per your requirements.

## See Also

*   [Compare Images in Java to Find Differences](https://blog.groupdocs.com/2021/06/16/compare-images-in-java/)
*   [Compare Excel, Word, PDF, or PowerPoint files in C#](https://blog.groupdocs.com/2020/03/10/compare-excel-word-pdf-files-in-csharp/)




