---
title: "3-fromsides"
css: "abcpdf-docs.css"
---

# FromSides Function

Creates an XRect from the coordinates of two diagonally opposite corners.

## Syntax

**[C#]**

```csharp
static XRect FromSides(double xMin, double yMin, double xMax, double yMax)
```

<span class=language>[Visual Basic]</span>  

              `Shared Function FromSides(xMin As Double, yMin As Double, xMax As Double, yMax As Double) As XRect`
## Params

| Name | Description | 
| --- | --- |
| xMin | The minimum x coordinate. | 
| yMin | The minimum y coordinate. | 
| xMax | The maximum x coordinate. | 
| yMax | The maximum y coordinate. | 

## Notes

This method constructs an XRect object from the coordinates of two diagonally opposite corners.

If the minimum x values are larger than the minimum x values then the XRect will have a negative width. Similarly if the minimum y values are larger than the maximum y values then the XRect will have a negative height.

## Example

None.