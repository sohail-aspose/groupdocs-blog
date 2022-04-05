---
title: 'Taxonomic Classification of Raw Text using C# - (IAB-2 &amp; Document Taxonomy)'
date: 
draft: true
url: /?p=23780
author: 'Shoaib Khan'
summary: ''
tags: ['Uncategorized']
---

In an article, we discussed how we can [analyze and classify complete documents programmatically](https://blog.groupdocs.com/2021/10/27/taxonomic-classification-of-documents-using-csharp/). It is often required to classify just some part of the document or only a few statements. In this article, we will identify the best possible taxonomic categories of the selected text. We will learn **how we can classify text according to IAB-2 and document taxonomies using C#**.

The following topics are covered below:

*   [.NET API for Taxonomic Classification](#text-classification-dotnet-api)
*   [Classify Text with IAB-2 Taxonomy](#classify-text-with-iab-2-taxonomy)
*   [Classify Text with Document Taxonomy](#classify-text-with-document-taxonomy)

## .NET API for Taxonomic Classification of Text {#text-classification-dotnet-api}

[GroupDocs.Classification for .NET](https://products.groupdocs.com/classification/) is the API that allows different techniques for the classification of text content within .NET applications. We will use this API to find the best possible taxonomic categories of the provided text using C# in examples.

You can download the **DLLs** or **MSI** installer from the [downloads section](https://downloads.groupdocs.com/classification/net) or install the API in your .NET application via [NuGet](https://www.nuget.org/packages/groupdocs.classification).

```
PM> Install-Package GroupDocs.Classification
```

## Text Classification with IAB-2 Taxonomy using C# {#classify-text-with-iab-2-taxonomy}

IAB-2 categorizes the content into defined [taxonomic categories](https://docs.groupdocs.com/classification/net/taxonomies/) and then classifies it based on the analysis. The following are the steps for taxonomic classification of text with [IAB-2 taxonomy](https://www.iab.com/guidelines/content-taxonomy/) using C#.

*   Instantiate the classifier using [Classifier](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier) class.
*   Define the text for taxonomic analysis.
*   Set the [Taxonomy](https://apireference.groupdocs.com/classification/net/groupdocs.classification/taxonomy) as **IAB2**.
*   Set the number of best results count as a result of classification. (_Optional_)
*   Get the taxonomic categories of the provided text by calling [Classify](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier/methods/classify/index) method with the defined parameters.
*   Print the [BestResults](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestresults) from the [classification response](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/index) of the Classify method.

The following C# source code shows how to classify text using **IAB-2 taxonomy** and get the top categories with the best match.

\[gist id="68adb40cdb317125614e04c8d1cf56b7" file="ClassifyTextWithIAB2Taxonomy.cs"\]```
 Class: Healthy\_Living,      Probability: 0.4144087
 Class: Medical\_Health,     Probability: 0.2108202
 Class: Science,                 Probability: 0.1584931
```

## Text Classification with Document Taxonomy using C# {#classify-text-with-document-taxonomy}

Documents taxonomy classifies the content into different [document classes](https://docs.groupdocs.com/classification/net/taxonomies/), such as advertisements, invoices, news, resume, letters, emails, etc. The following are the steps for taxonomic classification of text with document taxonomy using C#.

*   Instantiate the [Classifier](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier).
*   Load the text for taxonomic analysis.
*   Define the number of best results count as a result of classification. (_Optional_)
*   Set the [Taxonomy](https://apireference.groupdocs.com/classification/net/groupdocs.classification/taxonomy) as **Documents**.
*   Get the taxonomic groups by calling [Classify](https://apireference.groupdocs.com/classification/net/groupdocs.classification/classifier/methods/classify/index) method with the above defined parameters.
*   Print the [BestResults](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/bestresults) from the [classification response](https://apireference.groupdocs.com/classification/net/groupdocs.classification.dto/classificationresponse/properties/index) of the Classify method.

The following C# source code shows how to classify text content and get some of its top taxonomic categories using **document taxonomy**.

\[gist id="68adb40cdb317125614e04c8d1cf56b7" file="ClassifyTextWithDocumentTaxonomy.cs"\]```
 Class: ADVE,      Probability: 0.9999645
 Class: Report,     Probability: 3.461805E-05
```

## Get a Free License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, we learned to classify various kinds of documents using different taxonomies. In the examples, we classified the text as per IAB-2 and the document taxonomies using C#. After going through the series of posts, you can build your own .NET classification application to [classify documents](https://blog.groupdocs.com/2021/10/27/taxonomic-classification-of-documents-using-csharp/) as well as text with different taxonomies and configurations.

For more about the API, visit the [documentation](https://docs.groupdocs.com/classification). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Classify Customer's Feedback using Sentiment Analysis using C#](https://blog.groupdocs.com/2020/06/17/classify-customers-feedback-using-sentiment-analysis-in-csharp/)
*   [Taxonomic Classification of Documents using C#](https://blog.groupdocs.com/2021/10/27/taxonomic-classification-of-documents-using-csharp/)



