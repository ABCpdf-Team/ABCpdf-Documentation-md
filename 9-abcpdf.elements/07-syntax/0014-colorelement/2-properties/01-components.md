# Components Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | The component intensities for the color. | 

## Notes

The component intensities for the color. For example an RGB color has three values between zero and one, a CMYK color has four between zero and one.

Colors only make sense in the context of a color space that specifies what the components represent. Most components range between zero and one.

However some color spaces such as Lab have components with values outside this range.

## Example

None.