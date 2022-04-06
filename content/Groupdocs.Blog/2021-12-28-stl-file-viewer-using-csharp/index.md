---
title: 'STL File Viewer using C#'
date: Tue, 28 Dec 2021 11:00:00 +0000
draft: false
url: /2021/12/28/stl-file-viewer-using-csharp/
author: 'Shoaib Khan'
summary: 'STL (STereoLithography) file format is used for 3D CAD drawings and 3D printing. There are several requirements when the developers are required to programmatically render STL files into various other formats. One of the reasons for conversion is better portability. In this article, you will learn how to render the STL files into PDF format using C#. Additionally, we will convert the STL files to HTML, JPG, and PNG format within .NET application using examples.'
tags: ['STL as HTML', 'STL as JPG', 'STL as PNG', 'STL Viewer', 'STL Viewer using C#', 'View STL', 'View STL as PDF']
categories: ['GroupDocs.Viewer Product Family']
---

STL (**ST**ereo**L**ithography) file format is used for 3D CAD drawings and 3D printing. There are several requirements when the developers are required to programmatically render STL files into various other formats. One of the reasons for conversion is better portability. In this article, you will learn **how to render the STL files into PDF format using C#**. Additionally, we will convert the **STL files to HTML, JPG, and PNG format** within .NET application using examples.

The following topics are discussed below:

*   [STL Viewer .NET API](#stl-viewer-dotnet-api)
*   [View STL as PDF](#stl-to-pdf)
*   [View STL as HTML, JPG, PNG](#convert-stl-using-csharp)

## .NET API to View STL Files {#stl-viewer-dotnet-api}

[GroupDocs.Viewer](https://products.groupdocs.com/viewer/) showcases [document viewer .NET API](https://products.groupdocs.com/viewer/net/) that allows rendering the documents into PDF, HTML, and images within the .NET application. In this article, we will use it in examples to convert the STL files into different other file formats.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/viewer/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.viewer).

```
PM> Install-Package GroupDocs.Viewer
```

## View STL File as PDF using C# {#stl-to-pdf}

It is often required to convert the stereolithography STL format to PDF format due to its high portability. The following steps show how to convert the STL files into PDF format using C#.

*   Load the STL file using the [Viewer](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer) class.
*   Prepare the PDF rendering options using the [PdfViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/pdfviewoptions) class.
*   Use the [View()](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer/methods/view) method to render STL file as PDF.

The following C# code example renders the STL files into PDF format.

{{< gist GroupDocsGists 07d6814f87a48e2a208698b1dfeaab52 "ViewStlAsPdf.cs" >}}

## View STL File as HTML, JPG, or PNG using C# {#convert-stl-using-csharp}

Similarly, you can convert the STL files into other formats according to the requirement. The following steps help you to render the STL files into various other formats using C#.

*   Load the **STL** file using the [Viewer](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer) class.
*   Prepare the rendering options according to the conversion format:
    *   **HTML** rendering needs the [](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/pdfviewoptions)[HtmlViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/htmlviewoptions) class. (You can use either embedded or external resources)
    *   **JPG** rendering uses the [JpgViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/jpgviewoptions) class.
    *   **PNG** rendering requires the [PngViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/pngviewoptions) class.
*   Use the [View()](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer/methods/view) method to render STL file as HTML, JPG, or PNG.

Below are the C# examples that separately render STL files into each format using the respective format options.

### STL to HTML using C# {#stl-to-html}

The following C# code converts the STL file into HTML with embedded resources. Similarly, you can convert to HTML with external resources.

{{< gist GroupDocsGists 07d6814f87a48e2a208698b1dfeaab52 "ViewStlAsHtml.cs" >}}

### STL to JPG using C# {#stl-to-jpg}

The following C# code converts the STL file into JPG image format.

{{< gist GroupDocsGists 07d6814f87a48e2a208698b1dfeaab52 "ViewStlAsJpg.cs" >}}

### STL to PNG using C# {#stl-to-png}

The following C# code converts the STL file into PNG image format.

{{< gist GroupDocsGists 07d6814f87a48e2a208698b1dfeaab52 "ViewStlAsPng.cs" >}}

## Get a Free API License

You can use the APIs for free by [getting a temporary license](https://purchase.groupdocs.com/temporary-license).

## Conclusion

To conclude, we learned how to render the STL files into other formats. Specifically, we converted the STL files into PDF, HTML, JPG, and PNG formats using the C# example. You can build your own STL viewer application like [Groupdocs.Viewer Online App](https://products.groupdocs.app/viewer).

To learn more about [GroupDocs.Viewer for .NET](https://products.groupdocs.com/viewer/net/), visit its [documentation](https://docs.groupdocs.com/viewer/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Source Code to PDF in C#](https://blog.groupdocs.com/2021/12/03/convert-source-code-to-pdf-in-csharp/)
*   [View CAD Documents using C#](https://blog.groupdocs.com/2021/04/27/view-cad-documents-using-csharp/)
*   [Word Documents as HTML Responsive Page using C#](https://blog.groupdocs.com/2021/08/28/view-word-documents-as-html-responsive-page-using-csharp/)




