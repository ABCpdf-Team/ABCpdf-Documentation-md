---
title: "resize"
css: "abcpdf-docs.css"
---

# Resize Function

Resizes the rectangle.

## Syntax

**[C#]**

```csharp
void Resize(double w, double h)
void Resize(double w, double h, Corner corner)
```

<span class=language>[Visual Basic]</span>  

```
Sub Resize(w As Double, h As Double)
Sub Resize(w As Double, h As Double, corner as Corner)
```

## Params

| Name | Description | 
| --- | --- |
| w | The new width. | 
| h | The new height. | 
| corner | The corner to pin. | 

## Notes

Changes the width and height of the rectangle while maintaining the position.

When you change the width or height of a rectangle one corner of the rectangle is pinned to maintain position. The corner which is pinned is indicated by the [Pin](../2-properties/pin.md) property but you can override this default by specifying a corner when calling this function.

## Example

The following code.

[C#]

```csharp
var rc = new XRect();
rc.String = "20 20 220 120";
Response.Write($"Rect = {rc}");
Response.Write("&lt;br&gt;");
rc.Resize(50, 150);
Response.Write($"Pos. = {rc}");
```

<span class=language>[Visual Basic]</span>
```vbnet
Dim rc As New XRect()
rc.String = "20 20 220 120"
Response.Write($"Rect = {rc}")
Response.Write("&lt;br&gt;")
rc.Resize(50, 150)
Response.Write($"Pos. = {rc}")
```

Produces the following output.

Rect = 20 20 220 120Pos. = 20 20 70 170

Also see example code in: [ABCpdf Text Flow Round Image Example](../../../4-examples/02-textflow2.md).