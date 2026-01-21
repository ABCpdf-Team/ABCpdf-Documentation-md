---
title: "1-fromlbwh"
css: "abcpdf-docs.css"
---

# FromLbwh Function

Creates an XRect from a bottom left corner, a width and a height.

## Syntax

**[C#]**

```csharp
static XRect FromLbwh(double left, double bottom, double width, double height)
```

<span class=language>[Visual Basic]</span>  

              `Shared Function FromLbwh(left As Double, bottom As Double, width As Double, height As Double) As XRect`
## Params

| Name | Description | 
| --- | --- |
| left | The left coordinate. | 
| bottom | The bottom coordinate. | 
| width | The width of the rectangle. | 
| height | The height of the rectangle. | 

## Notes

This method constructs an XRect object from a bottom left corner, a width and a height.

It assumes that subsequent resizing and positioning operations on this object will also be based around the bottom left corner. As such the [Pin](../2-properties/pin.md) property will remain at its default of Corner.BottomLeft.

## Example

None.