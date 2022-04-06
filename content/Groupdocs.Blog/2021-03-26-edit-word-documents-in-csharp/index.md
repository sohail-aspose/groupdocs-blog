---
title: 'Edit Word Documents in C#'
date: Fri, 26 Mar 2021 09:42:00 +0000
draft: false
url: /2021/03/26/edit-word-documents-in-csharp/
author: 'Shoaib Khan'
summary: 'The most common and widely used word-processing file formats that are supported by Microsoft Word and OpenOffice Writer are DOC, DOCX, and ODT. We normally use these formats for drafting the documents. Therefore, as a developer, we widely need to edit Word documents in our applications programmatically. In this article, we will discuss how to edit Word documents in C# using the .NET API for document editing.'
tags: ['Edit DOCX in CSharp', 'Edit in CSharp', 'Edit Word doc in CSharp', 'Word Editing .NET API']
categories: ['GroupDocs.Editor Product Family']
---

The most common and widely used word-processing file formats are **DOC**, **DOCX**, and **ODT**. The famous Microsoft Word and OpenOffice Writer support these formats and we normally use these formats for drafting the documents. Therefore, as a developer, we widely need to edit Word documents in our applications programmatically. In this article, we will discuss **how to edit Word documents in C#** using the .NET API for document editing.

The following are the topics discussed briefly in this article:

*   [.NET API - Word Documents Editing](#word-editing-dotnet-api)
*   [Edit Word Documents in C#](#edit-word-docs-in-csharp)

## .NET API for Word Documents Editing and Automation {#word-editing-dotnet-api}

In this article, I will be using [GroupDocs.Editor for .NET](https://products.groupdocs.com/editor/net) in C# examples, which is the document editing API and allows developers to load, edit, and save various document formats using WYSIWYG HTML editors. In addition to the word-processing document formats, the API supports editing spreadsheets, presentations, HTML, XML, TXT, DSV, TSV, and CSV formats.

Download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/editor/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.editor).

```
PM> Install-Package GroupDocs.Editor
```

## Edit Word Documents in C# {#edit-word-docs-in-csharp}

Just after setting up the API, you can quickly move towards editing the Word document. The following steps will let you edit the word-processing document.

*   Load the Word document.
*   Edit accordingly with options.
*   Save the edited document.

### Load the Word document

Firstly, load the document by providing the document path and the password, if the document is protected.

```
using (FileStream fs = File.OpenRead(inputFilePath))
{
    Options.WordProcessingLoadOptions loadOptions = new WordProcessingLoadOptions();
    loadOptions.Password = "password-if-any";
}
```

### Edit the Word document

After loading, you can edit the loaded document as per your requirement. Here I am replacing all the occurrences of word "document" with the "edited document" in a Word document using the below C# code.

```
    using (Editor editor = new Editor(delegate { return fs; }, delegate { return loadOptions; }))
    {
        Options.WordProcessingEditOptions editOptions = new WordProcessingEditOptions();
        editOptions.FontExtraction = FontExtractionOptions.ExtractEmbeddedWithoutSystem;
        editOptions.EnableLanguageInformation = true;
        editOptions.EnablePagination = true;
        using (EditableDocument beforeEdit = editor.Edit(editOptions))
        {
            string originalContent = beforeEdit.GetContent();
            List<IHtmlResource> allResources = beforeEdit.AllResources;
            string editedContent = originalContent.Replace("document", "edited document");
        }
    }
```

### Save the Edited Word document with Options

Lastly, while saving the edited document content, you can further set various options. These options include; pagination, set password, locale, protection, or memory optimization settings. I set the above options in the below-mentioned code and save the edited document as a password-protected and read-only DOCX file.

```
using (EditableDocument afterEdit = EditableDocument.FromMarkup(editedContent, allResources))
{
    Options.WordProcessingSaveOptions saveOptions = new WordProcessingSaveOptions(WordProcessingFormats.Docx);
    saveOptions.EnablePagination = true;
    saveOptions.Locale = System.Globalization.CultureInfo.GetCultureInfo("en-US");
    saveOptions.OptimizeMemoryUsage = true;
    saveOptions.Password = "password";
    saveOptions.Protection = new WordProcessingProtection(WordProcessingProtectionType.ReadOnly, "write\_password");
    using (FileStream outputStream = File.Create("filepath/editedDocument.docx"))
    {
        editor.Save(afterEdit, outputStream, saveOptions);
    }
}
```

### Complete Code

For your convenience, I am showing the complete C# example that is explained above and it edits the Word document and then saves it in DOCX format.

{{< gist GroupDocsGists 3f18a8d8601ba835d6bd33991f42cbdd "EditWordDocument.cs" >}}

The following is the output document in which all the occurrences are replaced using the above code.



{{< figure align=center src="images/edited-document.png" alt="edited docx document using editor API" caption="Output document - All the occurrences are replaced">}}


## Conclusion

To conclude, we discussed editing Word documents in C# using document editing API for .NET applications. You can use the API with WYSIWYG editors for the visual editing of your documents. After that, you can move ahead to build your own document editor. Similarly, you can also integrate the editing feature within your .NET application.

For more details, options, and examples, you can visit the [documentation](https://docs.groupdocs.com/editor/net) and the [GitHub](https://github.com/groupdocs-editor) repository. For further queries, contact the support on the [forum](https://forum.groupdocs.com/c/assembly).

## Related Articles

*   [Edit XML files Data using C#](https://blog.groupdocs.com/2021/11/02/edit-xml-files-using-csharp/)
*   [How to Edit XML files in Java](https://blog.groupdocs.com/2021/11/06/edit-xml-files-in-java/)

## See Also

*   [On-Premise Document Editing APIs](https://products.groupdocs.com/editor/family)
*   [Document Editing and Automation Cloud APIs](https://products.groupdocs.cloud/editor/family)
*   [Edit Word Documents Online](https://products.groupdocs.app/editor/word)




