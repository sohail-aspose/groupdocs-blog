---
title: 'How to Password Protect and Remove Protection from Word Documents using C#'
date: Sat, 27 Nov 2021 04:30:16 +0000
draft: false
url: /2021/11/27/password-protect-word-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'Let us discuss how we can restrict the access to the Word documents by making them password protected. We have already learned to lock and unlock PDF, and PowerPoint files. In this article, we will see **how to password protect a Word document using C#**. Further, we will learn to **remove the password to unlock Word documents**, and lastly, **how to change the existing password of DOC & DOCX files** within the .NET applications.'
tags: ['add password in csharp', 'Change Doc Password in C#', 'Lock Files in CSharp', 'Lock Word Files in CSharp', 'Remove Password in CSharp', 'Unlock Files in CSharp']
categories: ['GroupDocs.Merger Product Family']
---

Let's discuss how we can restrict access to Word documents by making them password protected. We have already learned to [lock and unlock PDF](https://blog.groupdocs.com/2021/11/17/lock-unlock-pdf-files-with-password-using-csharp/), and [PowerPoint](https://blog.groupdocs.com/2021/11/25/lock-unlock-ppt-pptx-files-with-password-using-csharp/) files. In this article, we will see **how to password protect a Word document using C#**. Further, we will learn to **remove the password to unlock Word documents**, and lastly, **how to change the existing password of DOC & DOCX files** within the .NET applications.



{{< figure align=center src="images/lock-unlock-word-documents-in-dotnet.jpg" alt="Password Protect Word Documents using C#">}}


The following topics are discussed below:

*   [.NET API to Password Protect Word Documents](#dotnet-api-lock-unlock-documents)
*   [Add Password to Word Document](#password-protect-document)
*   [Change Password of Word Document](#change-password)
*   [How to Remove Password from Word Document](#remove-password-to-unlock)

## .NET API to Password Protect Word Documents {#dotnet-api-lock-unlock-documents}

[GroupDocs.Merger](https://products.groupdocs.com/merger/) provides the .NET API that allows locking and unlocking of Word documents within .NET applications. We will use [GroupDocs.Merger for .NET](https://products.groupdocs.com/merger/net/) to add, change, and remove password protection. In addition to protecting and unprotecting Word documents, there is much more that can be done with Word documents using the API. [Documentation](https://docs.groupdocs.com/merger/net/) is available that explains detailed features, supported file formats, and much more.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/merger) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.merger).

```
PM> Install-Package GroupDocs.Merger
```

## Password Protect Word Document in C# {#password-protect-document}



{{< figure align=center src="images/locked-DOC.jpg" alt="Programmatically Locked Word Doc">}}


Let's discuss how to add a password to word documents and make them password protected. The following steps show how to lock a word document (DOC/DOCX) with a password using C#.

*   Set the password options using the [AddPasswordOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/addpasswordoptions).
*   **Load** the document using the [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   **Add** the password to lock the loaded Word document using [AddPassword](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/addpassword) method.
*   **Save** the password protected file using the [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

The following code snippet shows how to password protect a Word document using C#.

{{< gist GroupDocsGists 3e111e3379902f9852f9e9d72308aeb1 "AddPasswordToDoc.cs" >}}

Now, when you try to open the password-protected document, the document viewer & editor will ask for the password to open the file.



{{< figure align=center src="images/enter-pwd-to-open-protected-word-doc.jpg" alt="Enter Password to Open Protected Word Document">}}


## Change Existing Password of Word Document in C# {#change-password}

Your old password might have been too common that has been guessed. Let's change it and be more careful next time. The following steps guide how to change the existing password of Word document using C#.

*   Prepare the [LoadOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/loadoptions) using the current password.
*   Define the [UpdatePasswordOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/updatepasswordoptions) using the new password.
*   **Load** the DOC/DOCX file using the [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   **Change** the password using the [UpdatePassword](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/updatepassword) method.
*   **Save** the protected document having new password using [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

Here is the C# code snippet that changes the existing password of a DOCX file.

{{< gist GroupDocsGists 3e111e3379902f9852f9e9d72308aeb1 "ChangeDocPassword.cs" >}}

## Remove Password from Word Document in C# {#remove-password-to-unlock}



{{< figure align=center src="images/unlocked-DOC.jpg" alt="Programmatically unlocked Word Document">}}


Now let's remove the protection from the documents that are no more confidential. First, open the Word document and then remove the password to make it unlocked. The following steps show how to unlock the Word document by removing the password using C#.

*   Use the document's existing password to prepare [LoadOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/loadoptions).
*   **Load** the Word document using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   **Remove** its password using [RemovePassword](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/removepassword) method.
*   **Save** the unlocked file in DOC/DOCX format by calling the [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

The following code sample unlocks the Word document of DOCX format by removing its password using C#

{{< gist GroupDocsGists 3e111e3379902f9852f9e9d72308aeb1 "RemoveDocPassword.cs" >}}

## Conclusion

Let's summarize what we learned today. Using a simple Word document, first, we made it password protected using C#. Next, we learned to change the existing password of a Word document. Lastly, we learned how to remove the password from the Word file to make it unlocked within any .NET application.

To learn more about **GroupDocs.Merger for .NET**, visit its [documentation](https://docs.groupdocs.com/merger) to start building your own document protector or password remover applications for various [supported document formats](https://docs.groupdocs.com/merger/net/supported-document-formats/). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## See Also

*   [Add & Remove Password Protection from PDF Files](https://blog.groupdocs.com/2021/11/17/lock-unlock-pdf-files-with-password-using-csharp/)
*   [Protect and Un-Protect PowerPoint Files](https://blog.groupdocs.com/2021/11/25/lock-unlock-ppt-pptx-files-with-password-using-csharp/)
*   [View Word Documents as HTML Responsive Page](https://blog.groupdocs.com/2021/08/28/view-word-documents-as-html-responsive-page-using-csharp/)
*   [Merge Word, PDF, Excel, PowerPoint Files](https://blog.groupdocs.com/2020/08/19/merge-pdf-word-excel-ppt-files-in-csharp/)
*   [Insert OLE Objects in Word, Excel, PowerPoint Files](https://blog.groupdocs.com/2020/05/16/insert-ole-objects-in-word-excel-powerpoint-with-csharp/)




