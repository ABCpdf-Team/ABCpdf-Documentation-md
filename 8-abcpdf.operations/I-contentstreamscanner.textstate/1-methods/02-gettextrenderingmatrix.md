---
title: "02-gettextrenderingmatrix"
css: "abcpdf-docs.css"
---

# GetTextRenderingMatrix Function

Get the current Text Rendering Matrix (Trm).

## Syntax

**[C#]**

```csharp
virtual XTransform GetTextRenderingMatrix(GraphicsState state)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function GetTextRenderingMatrix(state As GraphicsState) As XTransform`
			
## Params

| Name | Description | 
| --- | --- |
| state | The current graphics state. | 
| return | The Text Rendering Matrix. | 

## Notes

Get the current Text Rendering Matrix (Trm).

This transformation matrix encompasses all text state parameters and can be used to place text for output.

The Trm is part of the PDF Specification and is defined precisely in the documentation for this.

## Example

None.