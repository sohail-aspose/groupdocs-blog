---
title: 'Extract Data from Invoices and Receipts in Java'
date: Fri, 22 Jan 2021 16:48:00 +0000
draft: false
url: /2021/01/22/extract-data-from-invoices-or-receipts-in-java/
author: 'Shoaib Khan'
summary: 'In the era of online businesses, the use of digital invoices and receipts has largely increased. Similarly, the efficient data extraction from these digital invoices is also demanding. In this article, you will be knowing **how to extract data from PDF invoices or receipts programmatically in Java**.'
tags: ['data extraction from PDF invoices in Java', 'extract data from invoices in Java', 'extract data from PDF in Java', 'extract invoice data in Java', ]
categories: ['GroupDocs.Parser Product Family']
---

In the era of online businesses, the use of digital invoices and receipts has largely increased. Similarly, the efficient data extraction from these digital invoices is also demanding. In this article, you will be knowing **how to extract data from PDF invoices or receipts programmatically in Java**. Previously we have seen the [extraction of invoice data using C#](https://blog.groupdocs.com/2019/10/24/extract-data-from-invoices-or-receipts-in-csharp/) in one of the earlier posts.



{{< figure align=center src="images/Extract-Data-from-Invoices-using-GroupDocs.jpg" alt="Extract Data from PDF Invoices or Receipts">}}


## Document Parsing and Data Extraction Java API

I will be using [GroupDocs.Parser for Java](https://products.groupdocs.com/parser/java) to parse PDF invoices and extract data values within Java application. This API also allows extracting text, images, and metadata from documents, images, presentations, archives, email, and many other [supported document formats](https://docs.groupdocs.com/parser/java/supported-document-formats/).

### Download or Configure

From the [downloads section](https://downloads.groupdocs.com/parser/java), you may download the **JAR** file or just get the repository and dependency configurations for the pox.xml of your **maven-based** Java applications.

## How to Extract PDF Invoice Data in Java

The following steps will allow you to easily extract data from the PDF invoices using Java.

*   Create a template.
*   Parse the PDF invoice according to the created template.
*   Extract the information from the parsed PDF.

### Create Template for the Invoice

Below is the template that is created according to the invoice. You may also download the used invoice from the [sample files](https://github.com/groupdocs-parser/GroupDocs.Parser-for-Java/tree/master/Examples/Resources/SampleFiles) available at the GitHub repository.

{{< gist GroupDocsGists a10b693112f6d25dc1e9bcbea5211e88 "CreateTemplateForInvoice.java" >}}

### Parse PDF Invoice/Receipt for Data Extraction

The following lines will parse the PDF invoice according to the created template and extract the invoice data using simple Java code.

{{< gist GroupDocsGists a10b693112f6d25dc1e9bcbea5211e88 "ExtractDataFromInvoice.java" >}}

### The Output

The following is the output of the above code after extraction of data from the invoice.

```
**FROMCOMPANY:**    DEMO - Sliced Invoices
**FROMADDRESS:**    Suite 5A-1204
123 Somewhere Street
Your City AZ 12345
**FROMEMAIL:**     admin@slicedinvoices.com
**TOCOMPANY:**    Test Business
**TOADDRESS:**    123 Somewhere St
Melbourne, VIC 3000
**INVOICENUMBER:**             Invoice Number
**INVOICENUMBERVALUE:** NV-3337
**INVOICEORDER:**                Order Number
**INVOICEORDERVALUE:**    12345
**INVOICEDATE:**                    Invoice Date
**INVOICEDATEVALUE:**        January 25, 2016
**DUEDATE:**                           Due Date
**DUEDATEVALUE:**               January 31, 2016
**TOTALDUE:**                         Total Due
**TOTALDUEVALUE:**             $93.50
```

There are many other open-source examples available at [GitHub Repository](https://github.com/groupdocs-parser/GroupDocs.Parser-for-Java). You can download the code and quickly run the examples. For more guidance and some other ways to [use templates for parsing and data extraction in Java](https://docs.groupdocs.com/parser/java/working-with-templates/), visit the developer guide in the [documentation](https://docs.groupdocs.com/parser/java/introducing-groupdocs-parser-for-java/). In case of any further difficulty, reach the support team for free, any time on the [forum](https://forum.groupdocs.com/c/parser).

## See Also

*   [More about parsing PDF invoices in Java using templates](https://docs.groupdocs.com/parser/java/working-with-templates/)
*   [Extract Data from Invoices or Receipts in C#](https://blog.groupdocs.com/2019/10/24/extract-data-from-invoices-or-receipts-in-csharp/)




