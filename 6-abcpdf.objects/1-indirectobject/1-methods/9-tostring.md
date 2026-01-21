---
title: "9-tostring"
css: "abcpdf-docs.css"
---

# ToString Function

The string representation of the IndirectObject.

## Syntax

**[C#]**

```csharp
override string ToString()
```

<span class=language>[Visual
            Basic]</span>  
`Overrides Function ToString() As String`
## Params

| Name | Description | 
| --- | --- |
| return | The string representation of the object. | 

## Notes

This function derives the content of the object as it will be inserted into the final PDF document.

Note that the the string value of an object may be large and it may contain unusual characters.

## Example

None.