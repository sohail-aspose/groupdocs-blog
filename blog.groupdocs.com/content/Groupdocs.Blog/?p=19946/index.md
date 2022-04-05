---
title: 'Compare Images in Java'
date: 
draft: true
url: /?p=19946
author: 'Shoaib Khan'
summary: ''
tags: ['Uncategorized']
---

Whether you want to build an application with spot the difference feature or if you want to compare two images within any of your .NET based image processing applications, you are at the right place. After this article, you can easily compare JPG, PNG, BMP, or images with some other file formats. Without wasting time, let's compare images in C# using the [.NET API for document and image conversion](https://products.groupdocs.com/comparison/net).



{{< figure align=center src="images/compare-images-to-find-differences-in-dotnet.jpg" alt="Compare Images for Differences using .NET">}}


## .NET Image Comparison API

I will be using [GroupDocs.Comparison for .NET](https://products.groupdocs.com/comparison/net) API for comparing images in this article. This API supports comparing **JPG, PNG, BMP, DICOM, DCM, DjVu** images along with many other [supported file formats](https://docs.groupdocs.com/comparison/net/supported-document-formats/).

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/comparison/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.comparison).

```
PM> Install-Package GroupDocs.Comparison
```

## Compare Images to Highlight Differences using C#

Comparing two images in C# is too easy with GroupDocs.Comparison within .NET application. The following steps explain how we can compare any two JPG, PNG, BMP, or any other image.

*   Define the first image using the [Comparer](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer) class.
*   Add the second image using [Add](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/add/index) method of Comparer object.
*   Call [Compare](https://apireference.groupdocs.com/comparison/net/groupdocs.comparison/comparer/methods/compare/index) method to compare both the images and save the resultant image that highlights the differences among both the images.

The following C# code compares two JPG images and saves the output with differences.

\[gist id="d1153909e5e54a8c00ccd5ee422a450c" file="CompareImages.cs"\]

The above shown images on the left are used in this code, and the output is shown on the right side that highlights the differences.

## Conclusion

In this article, we have learned image comparison using C# with .NET API. Now you can build your own application to compare images and highlight the found differences.

To get a complete idea about the features of the API, you can go through the [Documentation](https://docs.groupdocs.com/comparison/net/). You may also contact the [Free Support Team](https://forum.groupdocs.com/c/comparison) or [Free Consulting Team](https://groupdocs-free-consulting.github.io/) that even writes code to help you understand the usage of GroupDocs APIs as per your requirements.

## See Also

*   [Compare Excel, Word, PDF or PowerPoint files in C#](https://blog.groupdocs.com/2020/03/10/compare-excel-word-pdf-files-in-csharp/)



