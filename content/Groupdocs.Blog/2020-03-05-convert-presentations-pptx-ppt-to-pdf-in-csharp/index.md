---
title: 'Convert PowerPoint PPT, PPTX and OpenOffice Presentations to PDF in C#'
date: Thu, 05 Mar 2020 21:59:00 +0000
draft: false
url: /2020/03/05/convert-presentations-pptx-ppt-to-pdf-in-csharp/
author: 'Shoaib Khan'
summary: '[PDF](https://wiki.fileformat.com/view/pdf/) is no doubt the [Portable Document Format](https://en.wikipedia.org/wiki/PDF), which is one of the most commonly used file formats. [PPT](https://wiki.fileformat.com/presentation/ppt/) and [PPTX](https://wiki.fileformat.com/presentation/pptx/) formats of Microsoft PowerPoint share the popularity in business documents. Due to the popularity of both the document formats and the fixed layout nature of PDF format, there comes the requirement to **convert PPT/PPTX to PDF** format.'
tags: ['Convert PPT to PDF in CSharp', 'Convert PPTX to PDF in CSharp', 'CSharp PPT to PDF', 'CSharp PPTX to PDF', ]
categories: ['GroupDocs.Conversion Product Family']
---

[PDF](https://wiki.fileformat.com/view/pdf/) is no doubt the [Portable Document Format](https://en.wikipedia.org/wiki/PDF), which is one of the most commonly used file formats. [PPT](https://wiki.fileformat.com/presentation/ppt/) and [PPTX](https://wiki.fileformat.com/presentation/pptx/) formats of Microsoft PowerPoint share the popularity in business documents. Due to the popularity of both the document formats and the fixed layout nature of PDF format, there comes the requirement to **convert PPT/PPTX to PDF** format.



{{< figure align=center src="images/Convert-PPT-to-PDF-csharp.png" alt="PPTX to PDF in C#">}}


Considering the .NET developers today, this article will be providing the solution to the above-mentioned file format conversion. GroupDocs supports the conversion of [50+ document formats](https://docs.groupdocs.com/conversion/net/supported-document-formats/), hence providing On-Premise APIs (.NET & Java), Cloud APIs, and online [Conversion Apps](https://products.groupdocs.app/conversion/family). After this article, you will get familiar with different ways to convert Microsoft and OpenOffice presentations using [GroupDocs.Conversion for .NET](https://products.groupdocs.com/conversion/net).

The following topics are discussed below:

*   [How to Convert Complete Presentation to PDF](#ppt-to-pdf)
*   [Convert Specific PPT slides to PDF](#specific-slides)
*   [Convert Sequential Subset of Slides to PDF](#successive-slides)
*   [Possible Conversions of PowerPoint PPT/PPTX format](#possible-conversions)
*   [Convert Presentation with Advanced Options](#ppt-to-pdf-adv)
*   [Apply Watermark while Conversion to PDF](#watermarked)

## Convert PPT to PDF in C# {#ppt-to-pdf}

[GroupDocs.Conversion](https://products.groupdocs.com/conversion) has made this so easy; the popular and demanding conversion of presentation files. Just with the below-mentioned two lines of CSharp code, you can quickly convert any type of presentation like PPTX or PPT to PDF.

*   Create a new instance of [Converter](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion/converter) Class with the source document.
*   Instantiate [PdfConvertOptions](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions) object.
*   Call [Convert()](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion/converter/methods/convert/2) method of Converter class.

The following code sample converts the complete PowerPoint PPTX to PDF in C#.

{{< gist GroupDocsGists 3b2358dd1dcdf2281bd21c0f01ceef0c "ConvertPptToPDF.cs" >}}

## Convert Specific Slides of PPT to PDF in C# {#specific-slides}

We could have a requirement to convert only the selected slides instead of converting the whole presentation. GroupDocs.Conversion allows converting the specific slides of a presentation to the resultant PDF document. Below are the steps and C# source code that shows, how to achieve this.

*   **Load** the presentation using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Prepare [ConversionOptions](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions) for PDF.
*   **List the selected slide numbers** to convert.
*   **Convert** to PDF using [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method.

The following source code converts slides number 1, and 3 of a presentation to PDF.

{{< gist GroupDocsGists 3b2358dd1dcdf2281bd21c0f01ceef0c "ConvertSpecifiedSlidesToPDF.cs" >}}

## Convert Consecutive Slides of PPTX to PDF using C# {#successive-slides}

With the little modification in the requirement, below is the little change in the code. Certain consecutive slides of the presentation can be selected to get these converted into PDF format. Just set the starting page number and number of successive pages ahead.

*   **Load** the presentation file using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Set the **starting page number** and the **count of sequentials slides** ahead using [PDF Conversion Options](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions).
*   **Save** the selected slides in PDF format using [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method.

The following code snippet converts the slide numbers 2, 3, and 4 to PDF format in C#.

{{< gist GroupDocsGists 3b2358dd1dcdf2281bd21c0f01ceef0c "ConvertConsecutiveSlidesToPDF.cs" >}}

## Possible Conversions of PPT/PPTX {#possible-conversions}

This is not only the PDF that could be the target document format while conversion. You can refer to the [documentation for all the possible conversions](https://docs.groupdocs.com/conversion/net/supported-document-formats/). More important for developers, we can retrieve all the possible conversion formats of PPT/PPTX presentations by simply calling the GetPossibleConversions() method of the Converter class.

*   Define the source format using the [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   Get all the possible conversions of the source format using [GetPossibleConversions()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/getpossibleconversions/index) method.

The following source code shows how to retrieve all the possible conversions of the PPTX formats using C#.

{{< gist GroupDocsGists 3b2358dd1dcdf2281bd21c0f01ceef0c "PossiblePptConversions.cs" >}}

## Convert PPT to PDF with Advanced Options {#ppt-to-pdf-adv}

There are many more options while converting the presentations. These options are rarely needed, however when required, they prove their importance.  [**PdfConvertOptions**](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions) gives control over conversion results while converting to PDF. Along with the common conversion options, it has many additional options that can be seen in detail from the [documentation](https://docs.groupdocs.com/conversion/net/convert-to-pdf-with-advanced-options/#ConverttoPDFwithadvancedoptions-PdfOptions). Just for an overview, we can customize the PPT conversion with the mentioned options and much more:

*   [Zoom](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfoptions/properties/zoom)
*   [Margins](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/marginleft)
*   [GrayScale](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfoptions/properties/grayscale)
*   [Formatting Options](https://docs.groupdocs.com/display/conversionnet/Convert+to+PDF+with+advanced+options#ConverttoPDFwithadvancedoptions-PdfFormattingOptions)
*   [Image Quality](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfoptimizationoptions/properties/imagequality)
*   [Rotation](https://apireference.groupdocs.com/net/conversion/groupdocs.conversion.options.convert/pdfconvertoptions/properties/rotate)
*   [Watermark](https://apireference.groupdocs.com/conversion/net)

{{< gist GroupDocsGists 3b2358dd1dcdf2281bd21c0f01ceef0c "PptToPdfAdvanced.cs" >}}

## Add Watermark while converting PPTX or PPT to PDF in C# {#watermarked}

Want to secure your presentation while converting it to PDF format? Leave a watermark on the resultant PDF. The below-mentioned steps and source code shows how to put a watermark when a PPT/PPTX presentation is converted to PDF format.

*   **Load** the PPT file using [Converter](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter) class.
*   **Prepare the [text watermark options](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/watermarktextoptions)** and define:
    
    *   Watermark Text & Font
    
    *   Watermark Color
    *   Widht and Height
    *   Rotation Angle
    *   Tranparency
*   **Add the prepared watermark** to [PDF conversion options](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion.options.convert/pdfconvertoptions).
*   **Save** the presentation to PDF using [Convert()](https://apireference.groupdocs.com/conversion/net/groupdocs.conversion/converter/methods/convert/index) method.

The following C# code example adds a watermark with rotation angle and transparency while converting the PPT to PDF.

{{< gist GroupDocsGists 3b2358dd1dcdf2281bd21c0f01ceef0c "WatermarkPPT.cs" >}}

## Conclusion

Let's summarize what we discussed. We learned different ways to convert PPT to PDF format in C#. We separately looked at the steps and code example for converting a **specific list of slides**, any **successive subset** of presentation slides, and conversion of **PPT to PDF with a customized watermark** and other options. Learn more about **GroupDocs.Conversion** from the [documentation](https://docs.groupdocs.com/conversion/net/).

## Let's Talk

You can build your own application using the above-highlighted features. We will be delighted if you contact us on the [forum](https://forum.groupdocs.com/c/conversion) to discuss, solve a problem, or share your feedback. Have a nice development time.

## See Also

*   [Convert PowerPoint and OpenOffice Presentations to PDF in Java](https://blog.groupdocs.com/2021/02/15/convert-presentations-odp-pptx-ppt-to-pdf-in-java/)




