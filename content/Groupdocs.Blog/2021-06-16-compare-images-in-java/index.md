---
title: 'Image Comparison in Java to Spot the Differences'
date: Wed, 16 Jun 2021 14:07:12 +0000
draft: false
url: /2021/06/16/compare-images-in-java/
author: 'Shoaib Khan'
summary: 'Worried! What is the difference? **Better automate the photo comparison.** In this article, we will discuss how to programmatically find differences between two images. After going through this, you will easily compare any images and highlight the identified differences using Java.'
tags: ['compare images in java', 'compare jpg in java', 'compare png in java', 'Image Comparison', 'Image Comparison Java API']
categories: ['GroupDocs.Comparison Product Family']
---

Worried! What's the difference? **Better automate the photo comparison.** In this article, we will discuss how to programmatically find differences between two images. After going through this, you will find it easy to compare any images and highlight the identified differences using Java.



{{< figure align=center src="images/images-for-comparison.jpg" alt="Identical Images for comparison">}}


The following topics are covered below:

*   [Java API for Comparing Images](#image-comparison-java-api)
*   [Compare Images in Java to Highlight Differences](#compare-image-and-highlight-differences)

## Images Comparison Java API {#image-comparison-java-api}

In this article, I will be using the [Java API of GroupDocs.Comparison](https://products.groupdocs.com/comparison/) for comparing images. Along with the most used image formats, like PNG, JPG/JPEG, and GIF, there is a [wide range of supported file formats for comparison](https://docs.groupdocs.com/comparison/java/supported-document-formats/). Additionally, the API allows the compare word-processing documents, spreadsheets, presentations, drawings, webpages, email messages, source code files, and much more.

### Download and Configure

Get the image comparison library from the [downloads](https://downloads.groupdocs.com/comparison/java) section. For Maven-based Java applications, add the following configuration within pom.xml. Later, you can try the examples of this article as well as many more from [GitHub](https://github.com/groupdocs-comparison). For the details, you may also visit the [API Reference](https://apireference.groupdocs.com/comparison/java).

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-comparison</artifactId>
        <version>21.6</version> 
</dependency>
```

## Compare Images in Java to Highlight Differences {#compare-image-and-highlight-differences}

Comparing the images and get the result is just 3 lines of code. You can follow the steps and use the mentioned source code for comparing any of your JPG, PNG, BMP, DICOM, DjVu, GIF, and other images. You can identify the dissimilarities or variations among these within the Java application.

The following steps show how any two images can be compared for differences.

*   Select the first image to compare using the [Comparer](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer) class.
*   Add the second image for comparison using the appropriate [add](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer#add(java.lang.String)) method.
*   Call the [compare](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer#compare(java.lang.String)) method to get the comparison result of both the images.

The following code shows how to compare two images in Java. It compares two JPG images and saves the output that highlights the identified differences.

{{< gist GroupDocsGists 65249752958d68af0cb507219d4ebe2d "CompareImages.java" >}}

Here is the output image of the above code. Additionally, the output also includes the summary of the comparison.



{{< figure align=center src="images/compared-image.jpg" alt="Image comparison automated and highlighted the differences">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To conclude from this article, we learned to compare images in Java. We further highlighted the identified differences after the comparison. Now you can build your own photo comparer app or use these features within your Java applications.

For more details, options, and examples, you can go through the [documentation](https://docs.groupdocs.com/comparison/java/) and [GitHub](https://github.com/groupdocs-comparison) repository. Reach us on the [forum](https://forum.groupdocs.com/) for your queries.

## See Also

*   [Compare images in C# to find the differences](https://blog.groupdocs.com/2021/01/06/compare-images-in-csharp-dotnet/)
*   [Compare any document using Java](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/)




