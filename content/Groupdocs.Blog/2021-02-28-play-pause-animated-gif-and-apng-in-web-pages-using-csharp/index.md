---
title: 'Play and Pause Animated GIF and APNG Images in Web Pages using C#'
date: Sun, 28 Feb 2021 12:52:00 +0000
draft: false
url: /2021/02/28/play-pause-animated-gif-and-apng-in-web-pages-using-csharp/
author: 'Shoaib Khan'
summary: '**GIF** and **APNG** are from the list of most common animated image formats. GIF stands for **G**raphics **I**nterchange **F**ormat and APNG files are the **A**nimated **P**ortable **N**etwork **G**raphics. If we compare GIF and APNG files of the same quality, it is noticed that APNG files are smaller in size. This article will be discussing to **play and pause animated GIF and APNG files in an HTML web page using C#**.

The following topics will be covered in this article:

*   .NET API for Animated Images
*   Play and Pause Animated APNG Image in HTML using C#
*   Play and Pause Animated GIF Image in HTML using C#'
tags: ['Play and Pause Animated Images', 'Play and Pause APNG in CSharp', 'Play and Pause GIF in CSharp', 'Render APNG to HTML in CSharp', 'Render GIF to HTML in CSharp']
categories: ['GroupDocs.Viewer Product Family']
---

**GIF** and **APNG** are from the list of most common animated image formats. GIF stands for **G**raphics **I**nterchange **F**ormat and APNG files are the **A**nimated **P**ortable **N**etwork **G**raphics. If we compare GIF and APNG files of the same quality, it is noticed that APNG files are smaller in size. This article will be discussing to **play and pause animated GIF and APNG files in an HTML web page using C#**.

The following topics will be covered below:

*   [.NET API for Animated Images](#dotnet-api-for-animated-images)
*   [Play and Pause Animated APNG Image in HTML using C#](#play-pause-animated-apng-in-csharp)
*   [Play and Pause Animated GIF Image in HTML using C#](#play-pause-animated-gif-in-csharp)

## .NET API for Animated Images {#dotnet-api-for-animated-images}

For the animated images, I will be using [GroupDocs.Viewer for .NET](https://products.groupdocs.com/viewer/net) API in the C# examples of this article. Along with the rendering of GIF and APNG images, this API supports rendering word-processing documents, spreadsheets, PDF, presentations, emails, ZIP archives, Visio and CAD drawings, eBooks images, programming source code files, and many other document formats.

You can download the DLLs or MSI installer from the [downloads section](https://downloads.groupdocs.com/viewer/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.viewer).

```
PM> Install-Package GroupDocs.Viewer
```

## Play and Pause Animated APNG Images in C# {#play-pause-animated-apng-in-csharp}

To render APNG image file to an HTML page, follow the below-mentioned steps. The C# souce code and output are also available below.

*   Create a [Viewer](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer) class object with the APNG image file.
*   Create the [HTMLViewOptions](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer.options/htmlviewoptions) object using **ForEmbeddedResources** method, and providing it the output HTML file.
*   Call the [View](https://apireference.groupdocs.com/viewer/net/groupdocs.viewer/viewer/methods/view/index) method of viewer object to create the view for the APNG animated image.

The following is the C# code that renders APNG image to HTML web page. It also provides the play and pause option for the animated PNG file.

{{< gist GroupDocsGists bf1680841cb8049c1d1162e8010113c9 "RenderApngWithPlayPause.cs" >}}

Here is the view of the output HTML page with the APNG file. From this link, you can also [experience the play and pause of APNG animation](https://blog.groupdocs.com/play-pause-apng.html) that is created using the above C# code.



{{< figure align=center src="images/play-pause-APNG-in-CSharp.gif" alt=" Pause APNG Animated PNG in C#">}}


## Play and Pause Animated GIF Images in C# {#play-pause-animated-gif-in-csharp}

If you want to render the GIF images to an HTML web page, you can do it using the similar code as above. The play and pause option will also be available for GIF animations as it is for APNG animations. The following C# code example renders the GIF animation file to HTML with the play and pause option.

{{< gist GroupDocsGists bf1680841cb8049c1d1162e8010113c9 "RenderGIFWithPlayPause.cs" >}}

## Conclusion

I am sure that you will be confident to give a try rendering animated GIF and APNG files to HTML web pages using C#. You can build your own .NET application having the feature to play and pause GIF and APNG animations in C#.

For more about the API and animated images, visit the [documentation](https://docs.groupdocs.com/viewer/net) or the open-source examples at [GitHub](https://github.com/groupdocs-viewer/GroupDocs.Viewer-for-.NET). Regarding any queries or confusion, feel free to contact support at the [forum](https://forum.groupdocs.com/c/viewer).

Have a nice Animated Day with C#.

## See Also

*   [CAD Documents Viewer using C# and Java](https://blog.groupdocs.com/2019/07/13/viewing-cad-documents/)




