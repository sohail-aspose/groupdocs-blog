---
title: 'GroupDocs Customer Newsletter – May 2015'
date: Fri, 01 May 2015 06:57:38 +0000
draft: false
url: /?p=6045
author: 'Stanislav Tatarin'
summary: ''
tags: ['Customer Newsletters', 'newsletter']
---

![](http://groupdocs.com/email/apr/separator-650px.png)

![](http://groupdocs.com/email/apr/separator-650px.png)

[![GroupDocs logo](http://groupdocs.com/email/apr/res/groupdocs-logo.png)](http://groupdocs.com)

Monthly Newsletter

May, 2015

Display 50+ Common Document Types on Your Kentico Site

Kentico is a popular CMS largely focused on document management. Recently we have released a plugin that allows Kentico developers to seamlessly integrate GroupDocs.Viewer for .NET library into their sites. With this integration, you can let your users view documents of all common business formats, including PDF and Microsoft Office, directly within your Kentico site all without having to install any Microsoft Office software.

[Find Out More](https://blog.groupdocs.com/display-pdf-microsoft-office-and-other-document-types-on-your-kentico-site)

![Document Viewer for Kentico](http://groupdocs.com/email/02-may-2015/1.png)

Product News

![](http://groupdocs.com/email/feb/separator-630px.png)

![](http://groupdocs.com/email/feb/product_news.png)

**GroupDocs.Viewer for .NET: improved search capability and streams handling API**

This month we have released two minor versions of the GroupDocs.Viewer for .NET library: [2.10.1](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_viewer_for_.net/entry5916.aspx) and [2.11.0](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_viewer_for_.net/entry6085.aspx). Each includes a number of fixes and optimizations, these include:

1\. Fixed behavior of the _SearchForSeparateWords_ method in the HTML-based rendering mode. Now if set to **true**, the viewer searches for and highlights all of the keywords specified in the search form, irrespective of the words order. Contrary, if the _SearchForSeparateWords_ method is set to **false**, then the viewer searches for the exact phrase specified in the search form.

2\. Previously, GroupDocs.Viewer tried to determine the document type by reading the signature at the beginning of the file. But this approach has shown to be problematic. In the latest GroupDocs.Viewer for .NET version we have implemented the **fileExtension** parameter as a mandatory _Stream_ method, which allowed us to remove the file type detection to make this functionality more reliable.

3\. Another API improvement was made to how the viewer generates stream names. Previously, GroupDocs.Viewer tried to generate a unique, but reproducible stream name by using its length. A more reliable approach could be to generate a hash of file contents. But it appeared to be very slow. As a result, we’ve removed the file name creation operation and set the _fileName_ parameter of the _Stream_ method as mandatory. For more details on this recent release and to download the library, please [visit this page](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_viewer_for_.net/entry6085.aspx).

**GroupDocs.Conversion for .NET: improved conversion accuracy**

In GroupDocs.Conversion for .NET version 1.9.0 we improved handling of complex objects when converting PDF files to Microsoft Word documents (e.g. tables with background colors and text within cells). Now you get even more accurate and clear results in the output of the “PDF to Word” conversion operations. In addition to that, accuracy was improved for the “XPS to TXT” and “PDF to JPEG” conversion operations. For more details on this recent release and to download the library, please visit [this page](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_conversion_for_.net/entry5933.aspx).

**GroupDocs.Total for Cloud: improved handling of documents loaded from URLs**

Several minor updates have also been implemented in GroupDocs.Total for Cloud. Among others, we would like to outline an enhancement that makes file loading from URLs more reliable. With this update we fixed an issue that in rare occurrences caused an error when trying to view a document loaded from the web.

From The Library

![](http://groupdocs.com/email/feb/separator-630px.png)

![](http://groupdocs.com/email/feb/from_the_library.png)

**GroupDocs.Viewer for .NET: working with the front-end using a JavaScript widget**

GroupDocs.Viewer for .NET comes with an out-of-the-box GUI that can be easily customized and embedded on your website. The GUI includes a number of controls that allow end users to easily navigate documents in a web-browser. To name a few, they are: download, print, search, rotate, zoom, view mode, page turning, etc. In this guide we list all JavaScript methods that allow developers to have complete control over widget’s behavior. [Go to the guide](http://groupdocs.com/docs/display/viewernet/Description+of+GroupDocs.Viewer+JavaScript+widget+methods).

**GroupDocs.Viewer for Java: getting started quickly**

GroupDocs.Viewer for Java can be downloaded in “slim" and "fat” packages. The “fat” one includes all required dependencies along with the library itself bundled in a single JAR, while the “slim” package includes the library only. Depending on your preferences, you can either use the “fat” package, or set all the required dependencies manually for the “slim” version. Whatever method you choose, please refer to [this page](http://groupdocs.com/docs/display/viewerjava/GroupDocs.Viewer+for+Java+-+Installation) for a detailed guide on how to install the library and download samples we’ve prepared to help you get started quickly.

Feedback

![](http://groupdocs.com/email/feb/separator-630px.png)

![](http://groupdocs.com/email/feb/feedback.png)

How Can We Help You?

Do you have ideas for what you'd like to see us do in 2015? [Take a minute to tell us](https://groupdocs.wufoo.com/forms/how-can-we-help-you/).

[![](http://groupdocs.com/email/feb/net.png?v)](http://groupdocs.com/dot-net)

[![](http://groupdocs.com/email/feb/java.png)](http://groupdocs.com/java)

[![](http://groupdocs.com/email/feb/cloud.png)](http://groupdocs.com/cloud)

[![](http://groupdocs.com/email/feb/apps.png)](http://groupdocs.com/apps)

Product Releases And Updates

![](http://www.aspose.com/Images/Newsletter/separator-630px.png)

[GroupDocs.Total for .NET:](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_total_for_.net/default.aspx) the latest versions of our .NET products packaged into one product suite.

 

[GroupDocs.Total for Java:](http://groupdocs.com/Community/files/9/java-libraries/groupdocs_total_for_java/default.aspx) the latest versions of our Java products packaged into one product suite.

[GroupDocs.Viewer for .NET 2.11.0:](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_viewer_for_.net/entry6085.aspx) improved search capability and streams handling API; other minor improvements.

 

[GroupDocs.Viewer for Java 2.9.1:](http://groupdocs.com/Community/files/9/java-libraries/groupdocs_viewer_for_java/entry5645.aspx) improved PPTX files rendering speed; minor improvements and bug fixes.

[GroupDocs.Comparison for .NET 2.3.3:](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_comparison_for_.net/entry5664.aspx) minor improvements and bug fixes.

 

 

[GroupDocs.Conversion for .NET 1.9.0:](http://groupdocs.com/Community/files/8/.net-libraries/groupdocs_conversion_for_.net/entry5933.aspx) improved “PDF to Word”, “XPS to TXT” and “PDF to JPEG” conversion accuracy; other minor improvements and bug fixes.



