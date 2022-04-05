---
title: 'Opening Remote Documents with GroupDocs.Viewer for .NET'
date: Wed, 28 Oct 2015 09:52:08 +0000
draft: true
url: /?p=6287
author: 'Denis Gvardionov'
summary: ''
tags: ['.net library', 'GroupDocs Viewer', 'zArchive']
---

[![GroupDocs.Viewer for .NET](https://blog.groupdocs.com/wp-content/uploads/sites/4/2014/04/GD_VWR_NETIcon_114.png)](http://groupdocs.com/dot-net/document-viewer-library)[GroupDocs.Viewer for .NET](http://groupdocs.com/dot-net/document-viewer-library) provides multiple options to open a document. Usually documents are stored in a form of files and are placed inside the root storage folder. Such documents should be pointed by using the **.FilePath()** method of the **ClientHelper** class, which is a main part of the GroupDocs.Viewer widget where all document- and display-related parameters are specified. When there is no way to get documents from files, they can be obtained in a form of byte streams. The **.Stream()** method is designed specifically for such cases. Please read [this article](https://docs.groupdocs.com/viewer/net) for more details on how to load documents from streams using GroupDocs.Viewer for .NET. But there may be cases when GroupDocs.Viewer is located on one machine, while the target document is located on another one and is available only as an HTTP resource via URL. If this is the case, you should use the **.Url()** method. In this article I’d like to discover how this method works and how to use it properly. I will also show you how to load remote documents when they are secured with the Windows Authentication protection. This is a common scenario in organizations with intranet where GroupDocs.Viewer is located on one machine, while documents – on another and can be accessed only via URLs. To read the article, please go to [this page](https://docs.groupdocs.com/viewer/net). If you have any questions or need help with this feature, please feel free to ask your questions on our [support forum](http://groupdocs.com/Community/Forums/Default.aspx).



