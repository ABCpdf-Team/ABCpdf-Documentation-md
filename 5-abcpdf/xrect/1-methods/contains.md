# Contains   Function

Determine if this rectangle contains a specified point or  rectangle.

## Syntax

[C#]

```csharp
bool Contains(<a href="../../xpoint/default.htm">XPoint</a> point)bool Contains(PointF point)bool Contains(Point point)bool Contains(float x, float y)bool Contains(double x, double y)bool Contains(<a href="../default.htm">XRect</a> rect)
```

[Visual Basic]

```vb
Function Contains(point As <a href="../../xpoint/default.htm">XPoint</a>) As BooleanFunction Contains(point As PointF) As BooleanFunction Contains(point As Point) As BooleanFunction Contains(x As Float, y as Float) As BooleanFunction Contains(x As Double, y as Double) As BooleanFunction Contains(rect As <a href="../default.htm">XRect</a>) As Boolean
```

## Params

| **Name** | **Description** |
| --- | --- |
| rect | The rectangle to test. |
| point | The point to test. |
| x | The x coordinate of a point to test. |
| y | The y coordinate of a point to test. |
| return | Whether the provided object is contained by this one. |

## Notes

Determine if this rectangle contains a specified point or rectangle.

In the case of rectangles, all four corners must be contained for the function to return true.

If a null point or rectangle is passed this function will return false.

## Example

None
