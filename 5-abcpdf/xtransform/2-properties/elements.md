# Elements Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp double[] ``` [Visual Basic] `Double()` | n/a | No | The transform as an array of floating-point values. | 

## Notes

The transform as an array of floating-point values.

Windows coordinates are measured in distances from the top left of the drawing surface while PDF coordinates are measured from the bottom left.

Remember that transforms operate on the underlying PDF coordinates rather than on any Windows coordinates. So by specifying a rotation around the origin you are specifying a rotation anchored at the bottom left of the document page.

## Example

None.