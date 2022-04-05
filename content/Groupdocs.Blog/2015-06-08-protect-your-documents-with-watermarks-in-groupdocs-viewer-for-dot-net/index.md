---
title: 'Protect Your Documents with Watermarks in GroupDocs.Viewer for .NET'
date: Mon, 08 Jun 2015 10:17:47 +0000
draft: false
url: /2015/06/08/protect-your-documents-with-watermarks-in-groupdocs-viewer-for-dot-net/
author: 'Denis Gvardionov'
summary: ''
tags: ['.net library', 'GroupDocs Viewer', 'watermarking', 'zArchive']
---

[![GroupDocs.Viewer for .NET](https://blog.groupdocs.com/wp-content/uploads/sites/4/2014/04/GD_VWR_NETIcon_114.png)](http://groupdocs.com/dot-net/document-viewer-library)One of the most requested and hence actively developed features in [GroupDocs.Viewer for .NET](http://groupdocs.com/dot-net/document-viewer-library) is watermarking. Watermarking allows you to protect documents that you display on the web from screen-grabbing. In GroupDocs.Viewer for .NET watermarks are implemented as customizable text that can be added over a displayed document, overlapping its content. For the first time the ability to add watermarks was implemented in GroupDocs.Viewer for .NET version 2.0. In its first implementation, the feature had a number of restrictions. In particular, watermarks could be used only in the image-based rendering mode and the only customization option was the ability to specify a text color. Since that time, a lot of new parameters have been added and, importantly, the watermarking feature is now available in the HTML-based rendering mode too. In this article I’d like to discover all new parameters of the watermarking feature we’ve added since its first implementation. But before we proceed with the parameters, I’d like to clarify several basic principles about how watermarks are rendered in GroupDocs.Viewer for .NET: 1. When adding watermarks, GroupDocs.Viewer doesn’t modify your original documents on the server. Instead, watermarks are rendered only on the client-side (over the document displayed in the GroupDocs.Viewer widget). So, be sure to disable the print and download options of your original files, or otherwise, end users will be able to get your documents without any watermarks. Alternatively, you can let users download and print PDF versions of the original files with watermarks burned in. More details about this option later in this article. 2. Watermarks are added to every page across the document. So far, you can’t add watermarks to specific pages only, or place different watermarks on different pages. 3. Watermarks, along with page rotation and reordering, are treated as one of the document modification features - they change representation of the document. But, unlike the page rotation and reordering options, watermark settings are not accessible from the client-side (GroupDocs.Viewer widget) and can’t be disabled or modified by viewers via the toolbar. We’re now ready to explore all parameters of the watermarking feature available to date. Let’s start with the method signature:```
public ClientHelper Watermark(
string watermarkText, 
Color? watermarkColor = new Color?(), 
WatermarkPosition watermarkPosition = 0, 
float watermarkWidthInPercents = 0f, 
bool printWithWatermark = false
)

```As you can see, the only mandatory parameter is **watermarkText** (you can’t add a textual watermark without actually specifying a text to display). All other parameters are optional, have default values and can be omitted. Now, let’s take a closer look at them: The **watermarkColor** parameter allows you to specify the color of the watermark text. The default color is red. You need to add a reference to the _System.Drawing.dll_ assembly for your project in order to be able to use the _System.Drawing.Color_ class. The **watermarkPosition** parameter in an enumeration which specifies a start position of the watermark. It allows you to specify the following values: Diagonal, TopLeft, TopCenter, TopRight, BottomLeft, BottomCenter and BottomRight. The default value - Diagonal – places text across the page starting from the bottom left corner to the top right corner. The **watermarkWidthInPercents** parameter requires a bit more clarification. By default, when this parameter is omitted, GroupDocs.Viewer tries to stretch the watermark text, making it as large as possible to match the page size. This default maximum size is treated as a 100% size. With this parameter you can decrease the watermark size, making the text smaller. The default value is "0" which equals 100%. A range from 1 to 99 (with support for fractional numbers) allows you to adjust the text size quite precisely. The **printWithWatermark** is the most interesting in this series. As you may already know, GroupDocs.Viewer can generate a PDF-version of the original document when users try to print (_.UsePdfPrinting(true)_) or download (_.DownloadPdfFileIfPossible(true)_) the displayed document. With the **printWithWatermark** parameter set to **true**, watermarks will be burned into the PDF copies of the original documents that end users print or download. This allows you to share any document in the PDF format, protected with your custom watermarks. That’s it. Hope the article answers all the questions you had about watermarking in GroupDocs.Viewer for .NET. If you still have any questions or experience issues when configuring watermarks, please feel free to ask for help on the GroupDocs [Support Forum](http://groupdocs.com/Community/Forums/Default.aspx).



