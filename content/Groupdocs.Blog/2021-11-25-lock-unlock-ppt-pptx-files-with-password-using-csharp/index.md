---
title: 'Lock &amp; Unlock PowerPoint Files with Password using C#'
date: Thu, 25 Nov 2021 15:48:29 +0000
draft: false
url: /2021/11/25/lock-unlock-ppt-pptx-files-with-password-using-csharp/
author: 'Shoaib Khan'
summary: 'Today, we will provide password protection to our presentation files programmatically. In this article, we will see **how to lock **PowerPoint presentation files** with password protection in C#**. Further, we will learn to unlock these by **removing the password** and also **how to change the existing password** of PPT & PPTX presentation files.

The following topics are discussed in this article:

*   .NET API to Protect PowerPoint PPT/PPTX with Password
*   Lock PowerPoint Files by adding Password
*   Change PPT/PPTX Password in C#
*   How to Remove PowerPoint Presentation Password'
tags: ['Add Password to PPT in CSharp', 'Change PPT Password in CSharp', 'Lock PPT in CSharp', 'Remove Password in CSharp', 'Unlock Files in CSharp']
categories: ['GroupDocs.Merger Product Family']
---

Today, we will provide password protection to our presentation files programmatically. Previously, we learned something similar while discussing [password protection of PDF files in C#](https://blog.groupdocs.com/2021/11/17/lock-unlock-pdf-files-with-password-using-csharp/). In this article, we will see **how to lock **PowerPoint presentation files** with password protection in C#**. Further, we will learn to unlock these by **removing the password** and also **how to change the existing password** of PPT & PPTX presentation files.



{{< figure align=center src="images/password-protect-lock-unlock-presentations.jpg" alt="Password Protect Presentations - Lock Unlock PPT-PPTX">}}


The following topics are discussed below:

*   [.NET API to Protect PowerPoint PPT/PPTX with Password](#lock-unlock-ppt-dotnet-api)
*   [Lock PowerPoint Files by adding Password](#lock-ppt-by-password)
*   [Change PPT/PPTX Password in C#](#change-ppt-password)
*   [How to Remove PowerPoint Presentation Password](#remove-password-to-unlock-ppt)

## .NET API to Lock and Unlock PowerPoint Files {#lock-unlock-ppt-dotnet-api}

To work with the protection of presentation files, we will use [GroupDocs.Merger for .NET](https://products.groupdocs.com/merger/net/). This API allows adding, changing, and removing password security features for the presentation and other documents within the .NET applications. Along with the locking and unlocking PPT files, the API provides many more features including merging and splitting presentations that are mentioned in the [documentation](https://docs.groupdocs.com/merger/net/).

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/merger) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.merger).

```
PM> Install-Package GroupDocs.Merger
```

## Add Password to PowerPoint Files in C# - Lock PPT/PPTX {#lock-ppt-by-password}



{{< figure align=center src="images/locked-PPT.jpg" alt="Lock PPT with Password">}}


We can programmatically lock any presentation file by adding password protection to it. The following steps show how to add a password to a PowerPoint presentation (PPT/PPTX) using C#.

*   Define the password using the [AddPasswordOptions](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/addpasswordoptions).
*   Load the PowerPoint file using the [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Apply protection by adding password using [AddPassword](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/addpassword) method.
*   Save the protected presentation file using the [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

The following C# code snippet locks the PPT by adding a password for limited access.

{{< gist GroupDocsGists 6b5a987cb0a752d6fdf3949108779561 "AddPasswordToPPT.cs" >}}

Here is the output of the above code. When you try to open the file, the editor or viewer will ask for the password to open the presentation.



{{< figure align=center src="images/enter-pwd-to-protected-pptx-presentation.png" alt="Enter Password to Protected PPTX">}}


## Update Existing Password of PPT/PPTX Files in C# {#change-ppt-password}

Looks like there was a sneak peek at your password. Let's change it. The following steps allow you to change the existing presentation file password using C#.

*   Prepare the [loading options](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/loadoptions) using the current password.
*   Prepare the [update options](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/updatepasswordoptions) using the new password.
*   Load the presentation using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   Change the password using the [UpdatePassword](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/updatepassword) method.
*   Call [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method to save the locked file having new password.

Here is the code snippet that changes the existing password of a PowerPoint PPT/PPTX presentation.

{{< gist GroupDocsGists 6b5a987cb0a752d6fdf3949108779561 "ChangePptPassword.cs" >}}

## Remove PowerPoint File Password in C# - Unlock PPT/PPTX {#remove-password-to-unlock-ppt}



{{< figure align=center src="images/unlocked-PPT.jpg" alt="Unlock PPT - Password Removed">}}


Now let's remove the cover and let everyone benefit from your presentation. First, open the file and then remove its password for easy access. The following steps show how to unlock the PPT file by removing its password using C#.

*   Use file's password to prepare the [loading options](https://apireference.groupdocs.com/merger/net/groupdocs.merger.domain.options/loadoptions).
*   **Load** the PowerPoint presentation document using [Merger](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger) class.
*   **Remove** the password using [RemovePassword](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/removepassword) method.
*   **Save** the unlocked file using the [Save](https://apireference.groupdocs.com/merger/net/groupdocs.merger/merger/methods/save/index) method.

The following C# code sample unlocks the PowerPoint presentation file by removing its password.

{{< gist GroupDocsGists 6b5a987cb0a752d6fdf3949108779561 "RemovePptPassword.cs" >}}

## Conclusion

Let's conclude with an overview of what we learned today. We used a simple PowerPoint presentation (PPTX) and first, we locked it just by adding a password. Next, we changed the existing password of the presentation file. Lastly, we learned how to remove the password of the PowerPoint presentations.

To learn more about GroupDocs.Merger for .NET, visit the [documentation](https://docs.groupdocs.com/merger) and start building your own application to lock and unlock presentation files. For queries, contact us via the [forum](https://forum.groupdocs.com/).

## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) to use the API without the evaluation limitations.

## See Also

*   [Lock & Unlock PDF Files with Password using C#](https://blog.groupdocs.com/2021/11/17/lock-unlock-pdf-files-with-password-using-csharp/)
*   [Convert PPT, PPTX Presentations to PDF in C#](https://blog.groupdocs.com/2020/03/05/convert-presentations-pptx-ppt-to-pdf-in-csharp/)
*   [Watermark PDF Files using C#](https://blog.groupdocs.com/2021/07/27/watermark-pdf-files-using-csharp/)
*   [How to Split PDF Files using C#](https://blog.groupdocs.com/2021/10/11/split-pdf-files-in-csharp/)




