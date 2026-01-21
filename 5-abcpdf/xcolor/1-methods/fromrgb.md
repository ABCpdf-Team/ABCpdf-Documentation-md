---
title: "fromrgb"
css: "abcpdf-docs.css"
---

# FromRgb Function

Create an XColor from a set of RGB component values.

## Syntax

**[C#]**

```csharp
static XColor FromRgb(int red, int green, int blue)
static XColor FromRgb(double red, double green, double blue)
```

<span class=language>[Visual
            Basic]</span>  

```
Shared Function FromRgb(red As Integer, green As Integer, blue As Integer) As XColor
Shared Function FromRgb(red As Double, green As Double, blue As Double) As XColor
```

## Params

| Name | Description | 
| --- | --- |
| red | The amount of red (0 to 255) | 
| green | The amount of green (0 to 255) | 
| blue | The amount of blue (0 to 255) | 
| return | The resulting XColor. | 

## Notes

Create an XColor from a set of RGB component values ranging between zero and 255..

## Example

None.