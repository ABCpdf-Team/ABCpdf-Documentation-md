---
title: "embeddedfile"
css: "abcpdf-docs.css"
---

# EmbeddedFile Function

EmbeddedFile Constructor

## Syntax

**[C#]**

```csharp
EmbeddedFile(ObjectSoup soup)
EmbeddedFile(ObjectSoup soup, string path)
EmbeddedFile(ObjectSoup soup, byte[] data)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub New(soup As ObjectSoup)
Sub New(soup As ObjectSoup, path As String)
Sub New(soup As ObjectSoup, data() As Byte)
```

## Params

| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created EmbeddedFile. | 
| path | A path to a file containing data which should be placed in the EmbeddedFile. | 
| data | An array of bytes which should be placed in the EmbeddedFile. | 

## Notes

Create an EmbeddedFile.

This constructor which takes a path to a file will embed and compress the file data using using the [CompressFlate](../../streamobject/1-methods/compressflate.md) function. It will also insert appropriate metadata using the [UpdateMetadata](updatemetadata.md) function.

The constructor which takes an array of data will similarly embed and compress the data. However since there is no file path metadata will not be assigned.

## Example

None.