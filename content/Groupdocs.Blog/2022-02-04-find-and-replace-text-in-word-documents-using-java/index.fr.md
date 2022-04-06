---
title: "Recherche de mots et remplacement de texte dans des documents Word à l'aide de Java"
date: Fri, 04 Feb 2022 15:24:00 +0000
draft: false
url: /fr/2022/02/04/trouver-et-remplacer-texte-dans-word-documents-en-utilisant-java/
author: 'Shoaib Khan'
summary: "Dans l'un des articles, nous avons déjà discuté de [comment expurger des mots dans des documents en tant que développeur .NET](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in- documents-utilisant-csharp/). La stratégie est utilisée de plusieurs façons pour effacer le contenu sensible, masquer ou supprimer des informations privées telles que les adresses e-mail ou les numéros d'identification. Cet article explique ** comment effectuer une recherche de mots dans les documents Word DOC/DOCX en Java. ** Nous discuterons séparément de la façon de ** rechercher et remplacer le texte, les mots ou les phrases ** avec différentes techniques utilisant l'API Java pour la rédaction."
tags: ['how to redact in word', 'how to redact PDF in Java', 'how to redact Word in Java', 'Java Redaction API', 'Redact in Java']
categories: ['GroupDocs.Redaction Product Family']
---

Dans l'un des articles, nous avons déjà discuté de [comment expurger des mots dans des documents en tant que développeur .NET](https://blog.groupdocs.com/2021/08/04/find-and-replace-text-in- documents-utilisant-csharp/). La stratégie est utilisée de plusieurs façons pour effacer le contenu sensible, masquer ou supprimer des informations privées telles que les adresses e-mail ou les numéros d'identification. Cet article explique ** comment effectuer une recherche de mots dans les documents Word DOC/DOCX en Java. ** Nous discuterons séparément de la façon de ** rechercher et remplacer le texte, les mots ou les phrases ** avec différentes techniques utilisant l'API Java pour la rédaction.

Les sujets suivants seront abordés ci-dessous :

* [API Java pour la recherche de mots et le remplacement de texte](#word-search-java-api)
* [Rechercher et remplacer des mots ou une expression](#replace-word-or-phrase)
* [Recherche de mots sensibles à la casse et remplacement de texte](#case-sensitive-text-redaction)
* [Remplacer le texte à l'aide d'expressions régulières (RegEx)](#replace-text-using-regex)
* [Remplacer le texte par une boîte de couleur](#hide-text-with-colored-box)

## API Java pour la recherche de mots et le remplacement de texte {#word-search-java-api}

**GroupDocs** fournit une [API de rédaction Java](https://products.groupdocs.com/redaction/java/) qui permet de rechercher et de remplacer le contenu des fichiers pris en charge par MS Word et d'autres documents de divers autres formats de fichiers. En plus de la rédaction et de la rastérisation du texte, l'API prend en charge les métadonnées, les annotations, les feuilles de calcul, ainsi que les fonctionnalités de rédaction des images. Les [formats de fichiers pris en charge](https://docs.groupdocs.com/redaction/java/supported-document-formats/) des documents Word, feuilles de calcul, présentations, images et documents PDF sont disponibles dans la documentation.

### Télécharger ou configurer

Vous pouvez télécharger le fichier **JAR** à partir de la [section des téléchargements](https://downloads.groupdocs.com/redaction), ou simplement obtenir les dernières configurations de référentiel et de dépendance pour le pox.xml de votre **maven- applications basées** sur Java.

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>https://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
<groupId>com.groupdocs</groupId>
<artifactId>groupdocs-rédaction</artifactId>
<version>21.12</version>
</dependency>
```

MS Word or any other third-party software is not required for the redaction process. Let’s now start with different approaches to deal with search and replace text. The following is the screenshot of a Word document that is used in the below examples. You can use the same methods for other document formats as well with very little or no change in the source code.



{{< figure align=center src="images/original-doc.png" alt="Document to redact text">}}


## Find and Replace Words or Phrase using Java {#replace-word-or-phrase}

The following steps explain how to find and then replace the occurrences of a word/phrase in a Word document within the Java application.

*   Load the DOC/DOCX file using [Redactor](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction/Redactor) class.
*   Find the exact phrase or word, using the [ExactPhraseRedaction](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/ExactPhraseRedaction) and [ReplacementOptions](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/ReplacementOptions) classes.
*   Use apply method of Redactor to apply redaction.
*   To save the file at different location after making changes, use the output stream.
*   Save the redaction changes using the [save](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction/Redactor#save(java.io.OutputStream,%20com.groupdocs.redaction.options.RasterizationOptions)) method.

The following code finds and replaces the word "John Doe" in the above Word document using Java. It replaces all the occurrences of “John Doe” with the word “\[censored\]”.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "ReplaceExactPhrase.java" >}}

The output of the code is as follows.



{{< figure align=center src="images/Exact-Phrase-Replacement.png" alt="Redact using Exact Phrase">}}


## Case-Sensitive Word Search and Replace Text in Java {#case-sensitive-text-redaction}

You seem cautious about the exact letter case of the word and only want to replace the word that only matches your case-sensitive search. The following code replaces the existence of the exact case match of the word “John Doe” in Java.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "ReplaceExactPhraseCaseSensitive.java" >}}

The output of the code is as follows.



{{< figure align=center src="images/Case-Sensitive-Exact-Phrase-Redaction.png" alt="Case sensitive redaction">}}


## Replace Text using Regular Expressions (RegEx) in Java {#replace-text-using-regex}

If you do not want to change the exact word but some pattern that exists in your document, you can use the Regular expressions. The following steps allow you to find and replace any pattern of text using regular expressions (RegEx) within your Java applications.

*   Load the document using [Redactor](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction/Redactor) class.
*   Create the RegEx using the [RegexRedaction](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/RegexRedaction).
*   Provide the text using [ReplacementOptions](https://apireference.groupdocs.com/redaction/java/com.groupdocs.redaction.redactions/ReplacementOptions) to replace the RegEx match.
*   Use apply method replace all the regex matches.
*   Use the save method to get the redacted document.

The following code shows how to perform the word search in a Word file using RegEx and replace it with some other text using Java.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "ReplaceTextWithRegEx.java" >}}

The following is the output of the above code:



{{< figure align=center src="images/Regex-Redaction.png" alt="RegEx Redaction">}}


## Replace the Text with Colored Box in Java {#hide-text-with-colored-box}

If you do not want to replace your content and just want to hide it, the API allows you to cover to text match by drawing a box over it. The following Java code hides the text with the black rectangle box.

{{< gist GroupDocsGists 567c29bb3a59ed182ff727aac4c24742 "FindTextAndHide.java" >}}

The output of the above code is as follows.



{{< figure align=center src="images/Colored-Box-Redaction.png" alt="Hide Text using Box">}}


## Get a Free API License

You can [get a free temporary license](https://purchase.groupdocs.com/temporary-license) in order to use the API without the evaluation limitations.

## Conclusion

To sum up, you learned how to perform word search to find text in Word documents using exact text phrase search, case-sensitive search, search using regular expressions, and last but not least hiding the text instead of replacing it. You can use these different techniques to replace the findings in different ways within MS Word documents.

For more details and learning about the API, visit the [documentation](https://docs.groupdocs.com/redaction). For queries, contact us via the [forum](https://forum.groupdocs.com/).

## See Also

*   [Build Full-Text Search Solution in Java](https://blog.groupdocs.com/2021/08/07/build-full-text-search-solution-in-java/)
*   [Image Comparison in Java to Spot the Differences](https://blog.groupdocs.com/2021/06/16/compare-images-in-java/)
*   [Rearrange Pages in Word using Java](https://blog.groupdocs.com/2022/03/01/move-word-pages-using-java/)
*   [Find and Replace Text in PDF using C#](https://blog.groupdocs.com/2022/02/19/find-and-replace-text-in-pdf-using-csharp/)





