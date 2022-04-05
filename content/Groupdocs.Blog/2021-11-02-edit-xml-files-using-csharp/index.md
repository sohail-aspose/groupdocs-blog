---
title: 'Edit XML Files using C#'
date: Tue, 02 Nov 2021 13:18:00 +0000
draft: false
url: /2021/11/02/edit-xml-files-using-csharp/
author: 'Shoaib Khan'
summary: 'XML is among the W3C recommended, structured formats, commonly used to store and transmit data. It is vastly required by developers to edit the stored XML data with the applications. To ease the requirement of editing, this article guides on **how to edit the XML file data using C#**.

*   XML Editing .NET API
*   How to Edit XML Files using C#'
tags: ['Edit XML File using C#', 'Edit XML in CSharp', 'How to Edit XML']
categories: ['GroupDocs.Editor Product Family']
---

XML is among the W3C recommended, structured formats, commonly used to store and transmit data. It is vastly required by developers to edit the stored XML data with the applications. To ease the requirement of editing, this article guides on **how to edit the XML file data using C#**.

*   [XML Editing .NET API](#xml-edit-dotnet-api)
*   [How to Edit XML Files using C#](#how-to-edit-xml)

## .NET API to Edit XML Files {#xml-edit-dotnet-api}

[GroupDocs.Editor](https://products.groupdocs.com/editor/) provides document editing solutions and APIs to [edit a large list of different file formats](https://docs.groupdocs.com/editor/net/supported-document-formats/). It is the .NET API that can be used along with external editors for visual editing. In this article, we will use GroupDocs.Editor for .NET for editing XML data within .NET application.

To download the **DLLs** or **MSI** installer, visit the [downloads section](https://downloads.groupdocs.com/editor) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.editor).

```
PM> Install-Package GroupDocs.Editor
```

## How to Edit XML Files using C# {#how-to-edit-xml}

Coming straight to the objective, we will modify the XML data by replacing a value with another. The following are the steps to edit or update the XML file using C#.

*   Load the XML data file using [Editor](https://apireference.groupdocs.com/editor/net/groupdocs.editor/editor) class.
*   Prepare the XML editing options using the [XmlEditOptions](https://apireference.groupdocs.com/editor/net/groupdocs.editor.options/xmleditoptions) class.
*   For editing, create the [EditableDocument](https://apireference.groupdocs.com/editor/net/groupdocs.editor/editabledocument) as source content using the [Edit](https://apireference.groupdocs.com/editor/net/groupdocs.editor/editor/methods/edit/index) method and the prepared editing options.
*   From the **EditableDocument**, get the original content of the XML file using [GetContent](https://apireference.groupdocs.com/editor/net/groupdocs.editor/editabledocument/methods/getcontent/index) method.
*   Update values in the XML content.
*   Now create a new **EditableDocument** from the updated XML content using [FromMarkup](https://apireference.groupdocs.com/editor/net/groupdocs.editor/editabledocument/methods/frommarkup) method.
*   For saving the updated content in different formats, prepare relevant saving options like [WordProcessingSaveOptions](https://apireference.groupdocs.com/editor/net/groupdocs.editor.options/wordprocessingsaveoptions) or [TextSaveOptions](https://apireference.groupdocs.com/editor/net/groupdocs.editor.options/textsaveoptions).
*   Save the updated XML data in any format using the [Save](https://apireference.groupdocs.com/editor/net/groupdocs.editor/editor/methods/save/index) method.

The following C# code snippet shows how to edit the XML file and update the data, later save it in any other format.

{{< gist GroupDocsGists d0ba38fe72fbf40caba648534764da59 "EditXML.cs" >}}

## Get a Free License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, we have learned to programmatically edit XML file data using C#. You can further explore other features of GroupDocs.Editor using the [documentation](https://docs.groupdocs.com/editor/net/). To clarify any ambiguity, contact us on the [forum](https://forum.groupdocs.com/c/assembly).

## See Also

*   [Edit XML files in Java](https://blog.groupdocs.com/2021/11/06/edit-xml-files-in-java/)
*   [How to Edit Word Documents in C#](https://blog.groupdocs.com/2021/03/26/edit-word-documents-in-csharp/)




