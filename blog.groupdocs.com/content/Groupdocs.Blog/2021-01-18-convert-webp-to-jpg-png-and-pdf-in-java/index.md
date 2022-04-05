---
title: 'Convert WebP to JPG, PNG, and PDF in Java'
date: Mon, 18 Jan 2021 22:52:00 +0000
draft: false
url: /2021/01/18/convert-webp-to-jpg-png-and-pdf-in-java/
author: 'Shoaib Khan'
summary: 'WebP images **give transparency like PNG**, **animate like GIF**, and the most important for any web developer is the **smaller size than comparative quality JPG format**. However, due to incompatibility issues or any other requirement, it is sometimes needed to convert the WebP image into JPG, PNG, or other formats.

While converting the WebP to JPG, PNG, or other formats, you can also apply color adjustments to the output images. You can change the contrast, brightness, and gamma of the resultant image. The Image can be flipped, rotated, apply watermarks, or get the grayscale image as the output.

[Continue Reading ...](https://blog.groupdocs.com/2021/01/18/convert-webp-to-jpg-png-and-pdf-in-java/)'
tags: ['convert WebP to JPG in java', 'Convert WebP to PNG in Java', 'Java Convert WebP', 'Java WebP to JPG', 'Java WebP to PDF', 'Java WebP to PNG']
categories: ['GroupDocs.Conversion Product Family']
---

WebP is the image format introduced by [Google](https://developers.google.com/speed/webp) that provides lossless and lossy compression for images on the web. WebP images are smaller in size as compared to the well-known and vastly used image formats like PNG and JPG, hence provides a faster web experience.



{{< figure align=center src="images/webp-to-jpg-converter-free-online.jpg" alt="Free Online WebP to JPG Converter">}}


_If you are here just to online convert your WebP files to JPG, PNG, or PDF documents, use the [free online WebP conversion tool by GroupDocs](https://products.groupdocs.app/conversion/webp-to-jpg) that is developed using GroupDocs.Conversion API. However, if you want to achieve the exact thing programmatically in Java, continue reading._

WebP images **give transparency like PNG**, **animate like GIF**, and the most important for any web developer is the **smaller size than comparative quality JPG format**. However, due to incompatibility issues or any other requirement, it is sometimes needed to convert the WebP image into JPG, PNG, or other formats.

*   [Java API to Convert WebP Images](#image-conversion-java-api)
*   [Convert WebP to JPG in Java](#convert-webp-to-jpg-in-java)
*   [Convert WebP to JPG, PNG, TIFF with Advanced Options in Java](#convert-webp-with-advanced-options-in-java)
*   [WebP to PDF Conversion in Java](#webp-to-pdf-conversion-in-java)



{{< figure align=center src="images/convert-webp-to-jpg-png-tiff-with-options.jpg" alt="Convert WebP image to JPG, PNG or PDF formats in Java and C#" caption="**The Original WebP image is changed to JPG format with color adjustments and options.** Image Used: [A Wild Cherry (Prunus avium) in flower](http://commons.wikimedia.org/wiki/File:Fr%C3%BChling_bl%C3%BChender_Kirschenbaum.jpg). Image Author: Benjamin Gimmel. Photo licensed under the [Creative Commons](http://en.wikipedia.org/wiki/en:Creative_Commons) [Attribution-Share Alike 3.0 Unported](http://creativecommons.org/licenses/by-sa/3.0/deed.en) license.">}}


## Java API to Convert WebP Images {#image-conversion-java-api}

GroupDocs provides the [solution](https://products.groupdocs.com/conversion) to convert 50+ document and image file formats. As a Java developer, you can use [GroupDocs.Conversion for Java](https://products.groupdocs.com/conversion/java) to convert WebP images within your Java-based applications.

You may download the **JAR** file from the [downloads section](https://downloads.groupdocs.com/conversion/java) or just add the following repository and dependency configurations in the pox.xml of your **maven-based** Java applications.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-conversion</artifactId>
        <version>20.10.3</version> 
</dependency>
```

While using GroupDocs.Conversion API, you can get the possible conversion formats of the source document or image by using the [getPossibleConversions()](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter#getAllPossibleConversions())  method of the [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter) class. There are several ways to get the possible conversions, you may visit the [documentation](https://docs.groupdocs.com/conversion/java/get-possible-conversions/) or the [API reference](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter#getPossibleConversions()) for this.

## Convert WebP to JPG in Java {#convert-webp-to-jpg-in-java}

The following steps help you convert the WebP image to JPG or other formats:

*   Initialize the [Converter](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion/Converter) class object with the WebP image file.
*   Set the conversion format to JPG using **setFormat** method of [ImageConvertOptions](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/ImageConvertOptions).
*   Convert the WebP to JPG using the convert method.

The below Java source code shows how easy is the WebP conversion to JPG format. For the conversion to some other supported formats, you just have to change the output format of the image by setting the appropriate ImageFileType. For instance, to convert WebP to PNG, just change the below ImageFileType from JPG to PNG.

{{< gist GroupDocsGists 6bfdc6033f28598a78631ccadf843c3c "ConvertWebPToJPG.java" >}}

## Convert WebP to JPG, PNG, TIFF with Advanced Options in Java {#convert-webp-with-advanced-options-in-java}

While converting the WebP to JPG, PNG, or other formats, you can also apply color adjustments to the output images. You can change the contrast, brightness, and gamma of the resultant image. The Image can be flipped, rotated, apply watermarks, or get the grayscale image as the output.

Above, I have shown the resultant images that are converted from WebP to JPG format after applying different variations using below mentioned Java code.

{{< gist GroupDocsGists 6bfdc6033f28598a78631ccadf843c3c "ConvertWebPWithAdvancedOptions.java" >}}

## WebP to PDF Conversion in Java {#webp-to-pdf-conversion-in-java}

Along with the conversion of WebP to other image formats, GroupDocs.Conversion API allows converting WebP into document formats like PDF as well. The following example shows how you can quickly convert WebP images into PDF (Portable Document Format). You can further apply different customization for the resultant PDF file using relevant [Convert Options](https://apireference.groupdocs.com/conversion/java/com.groupdocs.conversion.options.convert/package-frame).

{{< gist GroupDocsGists 6bfdc6033f28598a78631ccadf843c3c "ConvertWebPToPDF.java" >}}

There are many other open-source examples that are publicly available at [GitHub Repository](https://github.com/groupdocs-conversion/GroupDocs.Conversion-for-Java). Download the source code and quickly run the examples using the [getting started](https://docs.groupdocs.com/display/conversionjava/Getting+Started) guide. In case of any difficulty, look at the [documentation](https://docs.groupdocs.com/display/conversionjava/Home) or reach us at any time on the [forum](https://forum.groupdocs.com/c/conversion).

## Conclusion

I think, as a Java developer, you are now confident to programmatically convert the WebP images to JPG, PNG, GIF, TIFF, PDF, and other formats in Java. You can now easily change the color adjustment (contrast brightness, gamma, grayscale) to the converted formats and flip, rotate, or apply watermarks.

Why not create your own java-based application? It can convert the supported image format and apply different filters and color variations.

Have a nice coding day!

## See Also

*   [Convert WebP to JPG, PNG, TIFF, and PDF in C#](https://blog.groupdocs.com/2020/06/30/convert-webp-to-jpg-png-tiff-and-pdf-in-csharp/)




