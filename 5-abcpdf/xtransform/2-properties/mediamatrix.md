---
title: "mediamatrix"
css: "abcpdf-docs.css"
---

# MediaMatrix Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp MediaMatrix ``` [Visual Basic] `MediaMatrix` | n/a | No | The transform as a System.Windows.Media Matrix. | 

## Notes

The transform as a System.Windows.Media Matrix.

This matrix type holds elements as double precision floating point values.

Windows coordinates are measured in distances from the top left of the drawing surface while PDF coordinates are measured from the bottom left.

Remember that transforms operate on the underlying PDF coordinates rather than on any Windows coordinates. So by specifying a rotation around the origin you are specifying a rotation anchored at the bottom left of the document page.

## Example

None.