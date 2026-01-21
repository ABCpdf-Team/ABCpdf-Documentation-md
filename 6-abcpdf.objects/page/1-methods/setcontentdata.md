---
title: "setcontentdata"
css: "abcpdf-docs.css"
---

# SetContentData Function

Sets the content data for the page.

## Syntax

**[C#]**

```csharp
StreamObject SetContentData(byte[] buffer, bool compress)
StreamObject SetContentData(byte[] buffer, int index, int count, bool compress)
```

<span class=language>[Visual Basic]</span>  

```
Sub SetContentData(buffer() As Byte, compress As bool) As StreamObject
Sub SetContentData(buffer() As Byte, index As int, count As int, compress As bool) As StreamObject
```

## Params

| Name | Description | 
| --- | --- |
| buffer | The bytes containing the data to be set. | 
| compress | Whether the new stream should be Flate compressed. | 
| index | The byte offset in buffer, at which to begin copying bytes to the page contents. The default is zero. | 
| count | The number of bytes to be written to the page contents. The default is the buffer.Length. | 
| return | The stream containing the data. | 

## Notes

Sets the content data for the page.

You can specify a subset of the bytes in the array as the data for the content stream.

If the data for the current page is the same as that provided then nothing will be done and the existing stream will be returned.

## Example

None.