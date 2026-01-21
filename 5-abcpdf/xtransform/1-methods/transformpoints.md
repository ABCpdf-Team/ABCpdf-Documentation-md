---
title: "transformpoints"
css: "abcpdf-docs.css"
---

# TransformPoints Function

Applies this transform to a specified array of points.

## Syntax

**[C#]** ```csharp override Point[] TransformPoints(Point[] points) override PointF[] TransformPoints(PointF[] points) override XPoint[] TransformPoints(XPointF points) ``` [Visual Basic] ``` Overrides Sub TransformPoints(points As Point()) As Point[] Overrides Sub TransformPoints(points As PointF()) As PointF[] Overrides Sub TransformPoints(points As XPoint()) As XPoint[] ```

## Params

| Name | Description | 
| --- | --- |
| points | The array of points to be transformed. | 
| return | The array that was passed in. | 

## Notes

Applies this transform to a specified array of points.

The behavior of this method is the same as that of the System.Drawing.Drawing2D Matrix.TransformPoints function.

## Example