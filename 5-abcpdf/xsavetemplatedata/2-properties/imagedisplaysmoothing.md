# ImageDisplaySmoothing Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp RasterSmoothing ``` [Visual Basic] `RasterSmoothing` | Default | No | The smoothing for displaying images. | 

## Notes

This property specifies the smoothing for displaying images.

It can take any of the following values:

- Default – specifies the default algorithm.
- Alias – specifies no anti-aliasing.
- AntiAlias – specifies anti-aliasing.

Some output formats support different smoothing types for displaying images.

For SWF, this affects the FillStyleType field of the FILLSTYLE structure for images.

## Example

None.