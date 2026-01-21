---
title: "fromcmyk"
css: "abcpdf-docs.css"
---

# FromCmyk Function

Create an XColor given a set of CMYK component values.

## Syntax

**[C#]**

```csharp
static XColor FromCmyk(int cyan, int magenta, int yellow, int black)
static XColor FromCmyk(double cyan, double magenta, double yellow, double black)
```

<span class=language>[Visual
            Basic]</span>  

```
Shared Function FromCmyk(cyan As Integer, magenta As Integer, yellow As Integer, black As Integer) As XColor
Shared Function FromCmyk(cyan As Double, magenta As Double, yellow As Double, black As Double) As XColor
```

## Params

| Name | Description | 
| --- | --- |
| cyan | The amount of cyan (0 to 100) | 
| magenta | The amount of magenta (0 to 100) | 
| yellow | The amount of yellow (0 to 100) | 
| black | The amount of black (0 to 100) | 
| return | The resulting XColor. | 

## Notes

Create an XColor given a set of CMYK component values ranging between zero and 100.

## Example

None.