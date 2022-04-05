---
title: 'Extract RIFF INFO and Metadata of WAV files in Java'
date: Mon, 22 Mar 2021 16:37:44 +0000
draft: false
url: /2021/03/22/extract-riff-info-and-metadata-of-wav-files-in-java/
author: 'Shoaib Khan'
summary: '**RIFF** file container format used to store audio and video multimedia. This data stored in chunks can include lots of information such as the creation date, copyright information, artists, comments, etc. You can programmatically manipulate the metadata as well as RIFF INFO. This article guides developers to **programmatically extract metadata and RIFF INFO from the WAV audio files in Java**.

The following topics are covered in the article in brief:

*   Java API for Metadata Management
*   Extract Metadata of WAV Files in Java
*   Extract RIFF INFO of WAV Files in Java

[Continue Reading ...](https://blog.groupdocs.com/2021/03/22/extract-riff-info-and-metadata-of-wav-files-in-java)'
tags: ['extract metadata in java', 'Extract Metadata of WAV file in Java', 'Extract RIFF INFO of WAV in Java', ]
categories: ['GroupDocs.Metadata Product Family']
---

**RIFF** file container format used to store audio and video multimedia. This data stored in chunks can include lots of information such as the creation date, copyright information, artists, comments, etc. You can programmatically manipulate the metadata as well as RIFF INFO. This article guides developers to **programmatically extract metadata and RIFF INFO from the WAV audio files in Java**.

The following topics are covered in the article in brief:

*   [Java API for Metadata Management](#metadata-management-java-api)
*   [Extract Metadata of WAV Files in Java](#extract-metadata-of-wav-audio-in-java)
*   [Extract RIFF INFO of WAV Files in Java](#extract-riff-info-of-wav-audio-in-java)

## Java API for Managing Metadata and RIFF INFO {#metadata-management-java-api}

[GroupDocs.Metadata for Java](https://products.groupdocs.com/metadata/java) is the metadata automation and manipulation API for various document and image file formats. I will be using this API to extract metadata and RIFF INFO from WAV files. In addition to the audio WAV files, the API supports adding, removing, updating, and extracting metadata from **MP3 files** and **videos**. Furthermore, it also supports **Microsoft Office** and **Open Office** file formats, **eBooks**, **images**, and many other document formats.

### Download and Configure

[Get the library](https://downloads.groupdocs.com/metadata/java) from downloads or just add the following pom.xml configuration in your Maven-based Java applications to try the below-mentioned examples. For the details, you may visit the [API Reference](https://apireference.groupdocs.com/metadata/java).

```
<repository>
	<id>GroupDocsJavaAPI</id>
	<name>GroupDocs Java API</name>
	<url>http://repository.groupdocs.com/repo/</url>
</repository>
``````
<dependency>
        <groupId>com.groupdocs</groupId>
        <artifactId>groupdocs-metadata</artifactId>
        <version>21.2</version> 
</dependency>
```

## Extract Metadata of WAV Files in Java {#extract-metadata-of-wav-audio-in-java}

The following steps and the below-mentioned Java code example extract the metadata of the WAV files.

*   Load the WAV audio file.
*   Get the [WavRootPackage](https://apireference.groupdocs.com/metadata/java/com.groupdocs.metadata.core/WavRootPackage) of metadata.
*   Extract the [WavPackage](https://apireference.groupdocs.com/metadata/java/com.groupdocs.metadata.core/WavPackage) using _getWavPackage_ method.
*   Now you can access all the properties of WAV audio.

{{< gist GroupDocsGists 552bcf386d713c4751cde35ee85d043c "ExtractWavMetadata.java" >}}

The above code produces the following output with the provided wav file:

```
Bits per Sample: 16
Block Align: 4
Byte Rate: 176400
Number of Channels: 2
Audio Format: 1
Sample Rate: 44100
```

## Extract RIFF INFO of WAV Files in Java {#extract-riff-info-of-wav-audio-in-java}

If you want to extract the RIFF INFO of the WAV files, you can get it within your Java application using these steps. This is similar to the way we extracted the metadata shown above.

*   Load the WAV file.
*   Get the [WavRootPackage](https://apireference.groupdocs.com/metadata/java/com.groupdocs.metadata.core/WavRootPackage) of metadata.
*   Extract the [RiffInfoPackage](https://apireference.groupdocs.com/metadata/java/com.groupdocs.metadata.core/RiffInfoPackage) from the root package.
*   Now the properties of WAV audio are accessible.

The following code example extracts the RIFF INFO package metadata properties of the WAV file in Java.

{{< gist GroupDocsGists 552bcf386d713c4751cde35ee85d043c "ExtractWavRiffInfo.java" >}}

The following is the output of the above code:

```
Artist: GroupDocs 
Comment: Sample WAV File
Copyright: 
CreationDate: 2020-12-03
Software: Sound Forge
Engineer: SGEFFNER
Genre: Mystery
```

## Conclusion

In this article, we discussed how to programmatically extract metadata and RIFF INFO from WAV audio files in Java. I hope you find it quite simple. Now you can build your own metadata extractor Java application using GroupDocs.Metadata for Java.

## More about the API

*   [Documentation](https://docs.groupdocs.com/metadata/java/)
*   [Source code examples](https://github.com/groupdocs-metadata/GroupDocs.Metadata-for-Java)
*   [API Reference](https://apireference.groupdocs.com/metadata/java)

**Let’s clear any doubts @** [Free Support Forum.](https://forum.groupdocs.com/c/metadata)

## See Also

*   [Extract RIFF INFO and Metadata of WAV files in C#](https://blog.groupdocs.com/2021/03/05/extract-riff-info-and-metadata-of-wav-files-in-csharp/)
*   [Manage EXIF Data of Images in Java](https://blog.groupdocs.com/2020/05/12/handle-exif-data-of-jpg-png-webp-images-in-java/)




