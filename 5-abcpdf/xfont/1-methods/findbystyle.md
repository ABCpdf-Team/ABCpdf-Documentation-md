---
title: "findbystyle"
css: "abcpdf-docs.css"
---

# FindByStyle Function

Find a font from a specific family, with a given style.

## Syntax

**[C#]** ```csharp static XFont FindByStyle(string family, FontWeight weight, bool italic) static XFont FindByStyle(string family, int weight, bool italic) static XFont FindByStyle(IEnumerable fonts, int weight, int weightTolerance, bool italic) ``` [Visual Basic] ``` Shared Function FindByStyle(family As String, weight As FontWeight, italic As Boolean) As XFont Shared Function FindByStyle(family As String, weight As Integer, italic As Boolean) As XFont Shared Function FindByStyle(fonts As IEnumerable(Of XFont), weight As Integer, weightTolerance as Integer, italic As Boolean) As XFont ```

## Params

| Name | Description | 
| --- | --- |
| family | The name of the font family. | 
| fonts | The fonts. | 
| weight | The weight (or the midpoint of the permitted weight range) of the required font. | 
| weightTolerance | The maximum permitted difference between the weight parameter and the weight of the required font. The default value is 0. | 
| italic | Whether an italic font is required. | 
| return | A matching font. Null if no matching font could be found. | 

## Notes

This function finds a font from a specific family or among the given fonts, with a given style.

If no matching font can be found, then the function will return null.

The desired weight can be passed in either as an integer or as a value from the [FontWeight](../2-properties/weight.md) enumeration.

## Example

None.