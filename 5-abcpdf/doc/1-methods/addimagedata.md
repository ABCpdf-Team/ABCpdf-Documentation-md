---
title: "addimagedata"
css: "abcpdf-docs.css"
---

# AddImageData Function

Extract an image from data and add it to the current page.

## Syntax

**[C#]**

```csharp
int AddImageData(byte[] data)
int AddImageData(byte[] data, int frame)
```

<span class=language>[Visual
            Basic]</span>  

```
Function AddImageData(data() As Byte) As Integer
Function AddImageData(data() As Byte, frame As Integer) As Integer
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| data | The data containing the image in a format such as JPEG or TIFF. | 
| frame | Some image types support multiple frames or pages. This is the one based index specifying the required frame (default one). | 
| return | The ID of the newly added Image Object. | 

## Notes

Extract an image from a chunk of data and add it to the current page returning the ID of the newly added object.

This method is essentially the same as [AddImageFile](addimagefile.md) but it allows you add images specified as raw data rather than as a file path.

## Example

Also see example code in: [XRendering Overprint Property](../../xrendering/2-properties/overprint.md).