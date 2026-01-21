---
title: "settransform"
css: "abcpdf-docs.css"
---

# SetTransform Function

Set the transform.

## Syntax

**[C#]** ```csharp void SetTransform(double m11, double m12, double m21, double m22, double tx, double ty) void SetTransform(XTransform transform) ``` [Visual Basic] ``` Sub SetTransform(m11 As Double, m12 As Double, m21 As Double, m22 As Double, tx As Double, ty As Double) Sub SetTransform(transform As XTransform) ```

## Params

| Name | Description | 
| --- | --- |
| m11 | The new horizontal scale. | 
| m12 | The new vertical skew. | 
| m21 | The new horizontal skew. | 
| m22 | The new vertical scale. | 
| tx | The new horizontal translation. | 
| ty | The new vertical translation. | 
| transform | The source transform. | 

## Notes

This method sets the transform.

## Example