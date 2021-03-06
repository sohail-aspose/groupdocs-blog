---
title: 'Compare Text, Word, and PDF Files with Java Difference Library'
date: Wed, 15 Jul 2020 15:23:31 +0000
draft: false
url: /2020/07/15/compare-text-word-pdf-files-with-java-difference-library/
author: 'Shoaib Khan'
summary: 'After going through this article, we will be able to compare text files, Word files, PDF files, and other documents in Java-based applications. By using this feature, we can compare invoices, contracts, presentations, AutoCAD designs, price lists, or programming files. We will also the privilege to highlight the identified changes and have the option to either accept or reject any change. We can even build our own [document comparison tool](https://products.groupdocs.app/comparison/total) similar to the one launched by GroupDocs, using the document comparison API for Java.'
tags: ['compare PDF files in Java', 'compare two files using java', 'compare Word files in java', ]
categories: ['GroupDocs.Comparison Product Family']
---

After going through this article, we will be able to compare text files, Word files, PDF files, and other documents in Java-based applications. By using this feature, we can compare invoices, contracts, presentations, AutoCAD designs, price lists, or programming files. We will also the privilege to highlight the identified changes and have the option to either accept or reject any change. We can even build our own [document comparison tool](https://products.groupdocs.app/comparison/total) similar to the one launched by GroupDocs, using the document comparison API for Java.

Below, you will go through the following topics:

*   [Compare Word files and show differences](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/#compare-word-files).
*   [Compare Word files using streams](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/#compare-word-files-using-stream).
*   [Accept or reject the identified changes in Word file](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/#accept-or-reject-changes).
*   [Compare text files and highlight differences](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/#compare-text-files-in-java).
*   [Compare PDF files using Java](https://blog.groupdocs.com/2020/07/15/compare-text-word-pdf-files-with-java-difference-library/#compare-pdf-files-in-java).

## Java Document Comparison API

As a pre-requisite, you may get [GroupDocs.Comparison for Java](https://products.groupdocs.com/comparison/java) from the [downloads](https://downloads.groupdocs.com/comparison/java) section. Also, you can just add the following in your pom.xml in case of maven based applications:

### Repository```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
```

### Dependency```
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-comparison</artifactId>
        <version>20.4</version> 
</dependency>
```

## Compare Word Files and Show Differences using Java {#compare-word-files}

Steps below will show you to compare any two Word documents in just a few lines of Java code. As a result, you will get the resultant document that will be highlighting the identified changes.

*   Initialize the **[Comparer](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer)** object with the source document path.
*   Add the second document to compare using the **[add](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer#add(java.lang.String))** method.
*   Call the **[compare](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer#compare(java.lang.String))** method to get the result of the comparison. The compare method takes the name of the output document as a parameter.

```
// Compare two Word files from the provided location on disk
Comparer comparer = new Comparer("source.docx");
try {
    comparer.add("target.docx");
    comparer.compare("comparison.docx");
}
finally {
    comparer.dispose();
}
```

Here I am displaying the resultant Word document generated by the above code, and it contains the highlighted differences of the compared two Word documents. The deleted content will be marked in RED, added content will be displayed in Blue, however, Green shows the modified content.



{{< figure align=center src="images/word-files-text-comparison-using-java.png" alt="word-file-text-comparison-and-show-dirffer">}}


## Compare Word Files for Text using Stream {#compare-word-files-using-stream}

You can similarly pass the document as a stream to the Comparer class to get it compared with the second document. Here is the Java code to give you a clear idea:

```
// Compare two Word file using Stream
Comparer comparer = new Comparer(new FileInputStream("source.docx"));
try {
    comparer.add(new FileInputStream("target.docx"));
    comparer.compare(new FileOutputStream("result.docx"));
} 
finally {
    comparer.dispose();
}
```

## Accept or Reject the Compared Changes in Word File using Java {#accept-or-reject-changes}

After successfully highlighting the identified differences, you have the option to either accept or reject any change. Just to show as an example, I am accepting and rejecting the changes alternatively. You may display each change one by one with the similar code and take your decisions to accept/reject each change according to your requirement.

```
// Accept or Reject the identified changes of Word document in Java
Comparer comparer = new Comparer(source);
try {
    comparer.add(target);
    comparer.compare();
    ChangeInfo\[\] changes = comparer.getChanges();
    System.out.println("changes.length: " + changes.length + ".");
    // Accept or Reject the changes
    for (int n = 0; n < changes.length; n++) {
    	if (n % 2 == 0) {
    		changes\[n\].setComparisonAction(ComparisonAction.ACCEPT);
    	}
    	else {
    		changes\[n\].setComparisonAction(ComparisonAction.REJECT);
    	}
    }
    // Apply your decisions to get the resultant document.
    comparer.applyChanges(outputFileName, new SaveOptions(), new ApplyChangeOptions(changes));
}
finally {
    comparer.dispose();
}
```

## Compare Text Files and Show Differences using Java {#compare-text-files-in-java}

Using the Comparer class, we can also compare any text file. Below is the similar code for comparing two text files in Java. Steps are exactly the same as comparing any other two documents:

*   Start with passing the text file to the [Comparer](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer) class.
*   Add the second file using the [add](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer#add(java.lang.String)) method.
*   Call the [compare](https://apireference.groupdocs.com/comparison/java/com.groupdocs.comparison/Comparer#compare(java.lang.String)) method.

```
// Compare two text files to identify and highlight changes.
Comparer comparer = new Comparer("source.txt");
try {
    comparer.add("target.txt");
    comparer.compare("comparison.txt");
}
finally {
    comparer.dispose();
}
```

Here is the output document that shows the comparison result of matching two text files using the above code.



{{< figure align=center src="images/text-files-comparison-using-java.png" alt="Compare Text Files using Java">}}


## Compare PDF Files for Text Difference using Java {#compare-pdf-files-in-java}

We can compare the PDF files using the same above code, and by just changing the file extensions to ".pdf". Just to mention, the code below compare two pdf files and shows differences in Java.

```
// Compare two PDF file using Stream
Comparer comparer = new Comparer(new FileInputStream("source.pdf"));
comparer.add(new FileInputStream("target.pdf"));
comparer.compare(new FileOutputStream("result.pdf"));
```

Below is the outcome after comparing the PDF files.



{{< figure align=center src="images/pdf-files-text-comparison-using-java.png" alt="PDF File Text Comparison">}}


## See Also

*   [C# Diff Library for Comparing Text Files](https://blog.groupdocs.com/2020/04/30/groupdocs-comparison-for-net-c-sharp-diff-library-for-comparing-text-files/)
*   [Compare Two Files or More in C#](https://blog.groupdocs.com/2020/03/10/compare-excel-word-pdf-files-in-csharp/)

Many other open-source examples are publicly available at??[GitHub Repository](https://github.com/groupdocs-comparison/GroupDocs.Comparison-for-Java). You may download and quickly run the examples using the??[getting started](https://docs.groupdocs.com/comparison/java/getting-started/)??guide. In case of any query, look at the??documentation??or reach us at any time on the??[forum](https://forum.groupdocs.com/c/conversion).




