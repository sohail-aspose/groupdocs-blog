---
title: 'C# Diff Library for Comparing Text Files'
date: Thu, 30 Apr 2020 14:41:00 +0000
draft: false
url: /2020/04/30/groupdocs-comparison-for-net-c-sharp-diff-library-for-comparing-text-files/
author: 'Muhammad Sohail'
summary: 'The [GroupDocs.Comparison for .NET](https://products.groupdocs.com/comparison/net) is a C# library which allows you to compare documents and find differences. Compare and merge Microsoft Word, Excel, PowerPoint, OpenDocument, PDF, Text, HTML and [many other documents](https://docs.groupdocs.com/comparison/net), retrieve a list of changes between source and target document(s), apply or reject changes and save results with GroupDocs.Comparison API. In addition to this, GroupDocs.Comparison can identify styling and formatting changes - like bold, italic, underlines, strikethroughs, font types, etc.'
tags: ['compare text files', 'diff view library', 'GroupDocs Comparison', ]
categories: ['GroupDocs.Comparison Product Family']
---



{{< figure align=center src="images/groupdocs-comparison-128x128-1.png" alt="">}}


The [GroupDocs.Comparison for .NET](https://products.groupdocs.com/comparison/net) is a C# library which allows you to compare documents and find differences. Compare and merge Microsoft Word, Excel, PowerPoint, OpenDocument, PDF, Text, HTML and [many other documents](https://docs.groupdocs.com/comparison/net), retrieve a list of changes between source and target document(s), apply or reject changes and save results with GroupDocs.Comparison API. In addition to this, GroupDocs.Comparison can identify styling and formatting changes - like bold, italic, underlines, strikethroughs, font types, etc.

Changes detection algorithms used by [GroupDocs.Comparison](https://apireference.groupdocs.com/comparison/net) allows to detect differences in different document parts and blocks:

*   Text blocks - paragraphs, words and characters;
*   Tables;
*   Images;
*   Shapes etc.

Here are simple steps to compare two text files and show differences: 

*   Instantiate [Comparer](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer) object with source document path or stream;
*   Call [Add](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/add/index) method and specify the target document path or stream;
*   Call [Compare](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/compare/index) method.

The following code snippet demonstrates the simplest case of documents comparison using a couple lines of code. 

### Compare documents from local file```
using (Comparer comparer = new Comparer(“source.docx”))
{
    comparer.Add(“target.docx”);
    comparer.Compare(“result.docx”);
}
```

### Compare documents from the stream```
using (Comparer comparer = new Comparer(File.OpenRead(“source.docx”)))
{
    comparer.Add(File.OpenRead(“target.docx”));
    comparer.Compare(File.Create(“result.docx”));
}
```

Let's say you have two contracts in DOCX format that were concluded in different years. If you use the above code to compare these contracts, you get a DOCX file where the deleted elements are marked in red, the added in blue, and the modified in green as shown below:



{{< figure align=center src="images/FreelanceContract.png" alt="">}}


## Accept or Reject detected differences

[GroupDocs.Comparison](https://products.groupdocs.com/comparison/net) provides an ability to apply or discard specific changes between source and target documents and save the resultant document with (or without) selected changes.

The following are the steps to apply/reject changes to the resultant document.

*   Instantiate [Comparer](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer) object with source document path or stream;
*   Call _[A](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/add/index)_[dd](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/add/index) method and specify path target document path or stream;
*   Call [Compare](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/compare/index) method;
*   Call [GetChanges](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/getchanges/index) method and obtain detected changes list;
*   Set [ComparisonAction](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison.result/changeinfo/properties/comparisonaction) of needed change object to [ComparisonAction.Accept](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison.result/comparisonaction) or [ComparisonAction.Reject](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison.result/comparisonaction) value;
*   Call [ApplyChanges](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/applychanges/index) method and pass collection of changes to it.

The following code sample shows how to accept/reject detected differences.

```
using (Comparer comparer = new Comparer(“source.docx”))
{
    comparer.Add(“target.docx”);
    comparer.Compare();
    ChangeInfo\[\] changes = comparer.GetChanges();
    changes\[0\].ComparisonAction = ComparisonAction.Reject;
    comparer.ApplyChanges(File.Create(“result.docx”), new SaveOptions(), new ApplyChangeOptions() { Changes = changes });
}
```

## Generate document pages preview

[GroupDocs.Comparison](https://products.groupdocs.com/comparison/net) allows to generate page previews for source, target and resultant document(s) using [GeneratePreview](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/document/methods/generatepreview) method of a [Document](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/document) class.

[PreviewOptions](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison.options/previewoptions) class is used to manage preview generation process - specify desired page numbers, image format etc.

The following are the steps to generate a document preview with GroupDocs.Comparison API:

*   Create a new instance of [Comparer](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer) class and pass the source document path as a constructor parameter;
*   Add target document(s) to comparison using [Add](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/methods/add/index) method;
*   [Source](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/properties/source) and [Targets](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/properties/targets) properties of [Comparer](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer) object allows to access source and target documents and provides [GeneratePreview](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/document/methods/generatepreview) method;
*   Instantiate the [PreviewOptions](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison.options/previewoptions) object with:
    *   delegate for each page stream creation (see event handler CreatePageStream); 
    *   image preview format - PNG / JPG / BMP;
    *   page numbers to process;
    *   custom size of preview images (if needed).
*   Call [GeneratePreview](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/document/methods/generatepreview) method of [Source](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/properties/source) and [Targets](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison/comparer/properties/targets) document and pass [PreviewOptions](https://apireference.groupdocs.com/net/comparison/groupdocs.comparison.options/previewoptions) to it.

### Get page previews for resultant document```
using (Comparer comparer = new Comparer(“source.docx”))
{
    comparer.Add(“target.docx”);
    comparer.Compare(“result.docx”);
    Document document = new Document(File.OpenRead(“result.docx”));
    PreviewOptions previewOptions = new PreviewOptions(pageNumber =>
    {
        var pagePath = Path.Combine(“C:\\”, $"result\_{pageNumber}.png");
        return File.Create(pagePath);
    });
    previewOptions.PreviewFormat = PreviewFormats.PNG;
    previewOptions.PageNumbers = new int\[\] { 1, 2 };
    document.GeneratePreview(previewOptions);
}
```

## Compare multiple documents

[GroupDocs.Comparison](https://products.groupdocs.com/comparison/net) allows comparing more than two documents. The following code sample shows how to compare multiple documents programmatically.

```
using (Comparer comparer = new Comparer(“source.docx”)
{
    comparer.Add(“target1.docx”);
    comparer.Add(“target2.docx”);
    comparer.Add(“target3.docx”);
    comparer.Compare(“result.docx”);
}
```

## Installation

[NuGet](https://www.nuget.org/packages/GroupDocs.Comparison/) is the easiest way to download and install GroupDocs.Comparison for .NET. Please [get a temporary license](https://purchase.groupdocs.com/temporary-license) to test the library without any functional restrictions.

Please check the [documentation](https://docs.groupdocs.com/display/comparisonnet/Home) to learn more about the library. We also offer free technical support so please feel free to [contact us](https://forum.groupdocs.com/) - we will be happy to help.




