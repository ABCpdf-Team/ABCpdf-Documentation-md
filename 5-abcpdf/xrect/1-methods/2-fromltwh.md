---
title: "2-fromltwh"
css: "abcpdf-docs.css"
---

# FromLtwh Function

Creates an XRect from a top left corner, a width and a height.

## Syntax

**[C#]**

```csharp
static XRect FromLtwh(double left, double top, double width, double height)
```

<span class=language>[Visual Basic]</span>  

              `Shared Function FromLtwh(left As Double, top As Double, width As Double, height As Double) As XRect`
## Params

| Name | Description | 
| --- | --- |
| left | The left coordinate. | 
| top | The top coordinate. | 
| width | The width of the rectangle. | 
| height | The height of the rectangle. | 

## Notes

This method constructs an XRect object from a top left corner, a width and a height.

It assumes that subsequent resizing and positioning operations on this object will also be based around the top left corner. As such the [Pin](../2-properties/pin.md) property will be set to Corner.TopLeft.

## Example

None.