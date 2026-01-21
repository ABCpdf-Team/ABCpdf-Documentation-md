---
title: "datetostring"
css: "abcpdf-docs.css"
---

# DateToString Function

Convert a DateTime into a standard PDF date string.

## Syntax

**[C#]**

```csharp
static string DateToString(DateTime dateTime)
```

**[Visual Basic]**

`Shared Function DateToString(dateTime As DateTime) As String`
## Params

| Name | Description | 
| --- | --- |
| dateTime | The DateTime to be converted. | 
| return | The standard PDF date string. | 

## Notes

Convert a DateTime into a standard PDF date string.

The PDF date string covers date, time and time zone. The format is broadly similar to ASN.1 as detailed in ISO/IEC 8824.

For example, February 3, 2017, at 9:14 PM Pacific Standard Time would be represented as "D:201702032114-08'00".

## Example

None.