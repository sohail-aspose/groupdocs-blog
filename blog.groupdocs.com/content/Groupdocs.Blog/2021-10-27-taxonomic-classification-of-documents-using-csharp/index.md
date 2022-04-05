---
title: 'Taxonomic Classification of Documents using C# - (IAB-2 &amp; Document Taxonomy)'
date: Wed, 27 Oct 2021 12:24:00 +0000
draft: false
url: /2021/10/27/taxonomic-classification-of-documents-using-csharp/
author: 'Shoaib Khan'
summary: 'A classification is basically an approach in which text is systematically identified and then organized according to rules. Taxonomy defines the science of such classification. When you are dealing with a bunch of textual documents, it gets hard to find a topic of any document until the taxonomic classification of the content. In this article, you will learn **how to programmatically classify documents according to IAB-2 and document taxonomy using C#**.

The following topics are covered in this article:

*   .NET API for Taxonomic Classification
*   Document Classifcation with IAB-2 Taxonomy
*   Classify Documents with Document Taxonomy
*   Classify Password Protected Documents'
tags: ['Classify Documents using CSharp', 'Document Classification in CSharp', 'Document Taxonomy using CSharp', 'Taxonomic Classification using CSharp']
categories: ['GroupDocs.Classification Product Family']
---

A classification is basically an approach in which text is systematically identified and then organized according to rules. Taxonomy defines the science of such classification. When you are dealing with a bunch of textual documents, it gets hard to find a topic of any document until the taxonomic classification of the content. In this article, you will learn **how to programmatically classify documents according to IAB-2 and document taxonomy using C#**.

The following topics are covered below:

*   [.NET API for Taxonomic Classification](#document-classification-dotnet-api)
*   [Document Classifcation with IAB-2 Taxonomy](#classify-with-iab-2-taxonomy)
*   [Classify Documents with Document Taxonomy](#classify-with-document-taxonomy)
*   [Classify Password Protected Documents](#classify-secured-documents)

## .NET API for Taxonomic Classification of Documents {#document-classification-dotnet-api}

[GroupDocs.Classification](https://products.groupdocs.com/classification/) provides the classification solution for different kinds of applications. Its .NET API allows you to classify documents of various file formats according to different taxonomic categories within your .NET applications. We will use its [GroupDocs.Classification for .NET](https://products.groupdocs.com/classification/net/) API for the classification of PDF and Word documents using C#.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/classification/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.classification).

```
PM> Install-Package GroupDocs.Classification
```

## Classify Documents with IAB-2 Taxonomy using C# {#classify-with-iab-2-taxonomy}

IAB-2 categorizes the document's content into multiple [topics](https://docs.groupdocs.com/classification/net/taxonomies/) and then classifies it based on the depth level. The following are the steps to identify the taxonomic classification of documents with [IAB-2 taxonomy](https://www.iab.com/guidelines/content-taxonomy/) using C#.

*   Instantiate the classifier using [Classifier](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier) class.
*   Define the input document and input folder.
*   Define the [Taxonomy](https://apireference.groupdocs.com/classification/net/groupdocs.classification/taxonomy) as **IAB2**.
*   Set the count for the first few best results in the response. (_Optional_)
*   Get the taxonomic categories by calling [Classify](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier/methods/classify/index) method with the defined parameters.
*   Print the [Best Class Name](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestclassname) and [Probability](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestclassprobability) using the [classification response](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/index) of the Classify method.

The following C# source code shows how to classify documents using **IAB-2 taxonomy** and get some of the top document classification results.

{{< gist GroupDocsGists ca2a11f8c02562c2a73f419451115fa1 "ClassifyDocsWithIAB2Taxonomy.cs" >}}```
 Class: Technology\_&Computing,     Probability: 0.8188434 
 Class: Video\_Gaming,                     Probability: 0.12686 
 Class: Hobbies&\_Interests,             Probability: 0.03112753 
 Class: Music\_and\_Audio,                Probability: 0.006756512
```

## Classify Documents with Document Taxonomy using C# {#classify-with-document-taxonomy}

Documents taxonomy is used to identify different [document classes](https://docs.groupdocs.com/classification/net/taxonomies/), such as Invoices, CVs, forms, emails, etc. The following are the steps to identify the taxonomic classification of documents with document taxonomy using C#.

*   Instantiate the classifier using [Classifier](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier) class.
*   Set the input document and folder.
*   Define the [Taxonomy](https://apireference.groupdocs.com/classification/net/groupdocs.classification/taxonomy) as **Documents**.
*   Set the count for the number of top results in the response. (_Optional_)
*   Get the taxonomic groups by calling [Classify](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier/methods/classify/index) method with the above defined parameters.
*   Print the [Best Class Name](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestclassname) and [Probability](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestclassprobability) using the [classification response](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/index) of the Classify method.

The following C# source code shows how to classify documents and get some of the best taxonomic categories using **document taxonomy**.

{{< gist GroupDocsGists ca2a11f8c02562c2a73f419451115fa1 "ClassifyDocsWithDocumentTaxonomy.cs" >}}```
 Class: ADVE,         Probability: 0.3874436
 Class: Resume,     Probability: 0.2438204
 Class: News,         Probability: 0.1357582
 Class: Memo,        Probability: 0.0641943
```

## Classify Password Protected Documents using C# {#classify-secured-documents}

If your document is secured with a password, you can just provide the credentials while classifying. The following are the steps for the classification of password-protected documents using C#

*   Instantiate the [Classifier](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier).
*   Define the input document, input folder, and password of the protected document.
*   Define the [Taxonomy](https://apireference.groupdocs.com/classification/net/groupdocs.classification/taxonomy) as **Documents**.
*   Get the taxonomic group by calling [Classify](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier/methods/classify/index) method with the defined parameters.
*   Get the [Best Class Name](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestclassname) and [Probability](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestclassprobability) from the [response](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/index) of the Classify method.

The following code snippet shows how to classify password-protected documents and get the best taxonomic category using the default taxonomy (IAB-2).

{{< gist GroupDocsGists ca2a11f8c02562c2a73f419451115fa1 "ClassifyPasswordProtectedDocuments.cs" >}}```
Best Class: Hobbies\_&\_Interests,      Probability: 0.4548415
```

The default values for the taxonomy would be IAB-2 and the count of the best results would be 1.

## Get a Free License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude, we learned to classify various kinds of documents using different taxonomies. More precisely, we classified PDF documents as per IAB-2 and document taxonomies using C#. Further, we discussed how we can classify password-protected Word documents with default or specific taxonomic classification. Now you can integrate the document classification feature within your .NET application.

For more about the API, visit the [documentation](https://docs.groupdocs.com/classification). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Classify Text with IAB-2 & Document Taxonomy using C#](https://blog.groupdocs.com/2021/10/31/taxonomic-classification-of-text-using-csharp/)
*   [Classify Customer's Feedback using Sentiment Analysis using C#](https://blog.groupdocs.com/2020/06/17/classify-customers-feedback-using-sentiment-analysis-in-csharp/)




