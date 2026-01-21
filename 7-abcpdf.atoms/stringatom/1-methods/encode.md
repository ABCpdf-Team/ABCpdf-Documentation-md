---
title: "encode"
css: "abcpdf-docs.css"
---

# Encode Function

Encode a string into a format for use in a content stream using a normal or simple font.

## Syntax

**[C#]**

```csharp
static StringBuilder Encode(string text, IDictionary encoding, StringBuilder builder)
```

**[Visual Basic]**

`Shared Function Encode(text As String, encoding As IDictionary, builder As StringBuilder) As StringBuilder`
## Params

| Name | Description | 
| --- | --- |
| text | The text to be encoded. | 
| encoding | The encoding to use - typically obtained from the FontObject.GetEncoding method. | 
| builder | The StringBuilder to which the encoded representation should be appended. | 
| return | The updated StringBuilder. | 

## Notes

Encode a string into a format for use in a content stream using a normal or simple font.

Typically you will obtain an appropriate encoding from the FontObject.GetEncoding method. This method supports eight bit characters only as this is what is supported by simple fonts. Most commonly you will want to use the Latin horizontal encoding.

You should not use a null or identity encoding as there are subtle differences between the Latin1 encoding used in PDF and the first 256 characters of Unicode. As such if you use a null or identity encoding then characters such as the Euro sign will appear incorrectly.

## Example

None.