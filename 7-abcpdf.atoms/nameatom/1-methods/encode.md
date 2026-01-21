---
title: "encode"
css: "abcpdf-docs.css"
---

# Encode Function

Encode text into a PDF name.

## Syntax

**[C#]**

```csharp
string Encode(string value)
```

<span class=language>[Visual
            Basic]</span>  

            `Function Encode(value As String) As String`
## Params

| Name | Description | 
| --- | --- |
| value | The text to convert. | 
| returns | The string representation. | 

## Notes

Encode text into a PDF name.

PDF names contain restrictions on the types of characters that can be contained. Reserved characters may need to be escaped.

This function allows you to convert a string into a name format which can be directly inserted into a PDF or content stream.

## Example

None.