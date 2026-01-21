---
title: "getdata"
css: "abcpdf-docs.css"
---

# GetData Function

Get the raw binary content of the stream.

## Syntax

**[C#]**

```csharp
byte[] GetData()
byte[] GetData(bool decompress)
```

**[Visual Basic]**

```
Function GetData() As Byte()
Function GetData(decompress As Boolean) As Byte()
```

## Params

| Name | Description | 
| --- | --- |
| decompress | Whether the data should be decompressed. Default false. | 
| return | The raw binary content of the stream. | 

## Notes

Get the raw binary content of the stream.

This method does not alter the content of the StreamObject so it is an efficient way of getting the data without altering the document.

If decompression is requested but could not be performed, then an exception will be raised. This can occur if the source data is corrupt.

## Example

None.