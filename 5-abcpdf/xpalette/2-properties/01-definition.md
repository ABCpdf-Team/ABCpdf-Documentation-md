# Definition Property

## Notes

The set of colors that may be used.

The PaletteDefinition enumeration may take the following values:

An Adaptive palette uses a scan through the image to determine a good set of colors based on those most commonly used. It aims to produce a palette with Size colors. However it may use fewer colors than specified if the image has limited colors. This is the default option and the one you will most commonly want to use. Use in conjunction with the FixedColors property to ensure that colors like black and white are always present.

WebSafe, Windows and Macintosh palettes are all fixed sets of 256 colors. For this reason the Size and FixedColors properties are ignored.

Uniform sets of colors exist for 8, 27, 64, 125 and 216 colors and so the number of colors used may be less than the Size you specify. The FixedColors property is ignored.

Grayscale palettes uses the exact number of gray values specified using the Size with a minimum of two. The FixedColors property is ignored.

Black&White palettes always uses two colors - black and white. The FixedColors property is ignored.

Exact palettes are very similar to Adaptive palettes except they are optimized to ensure an exact color match wherever possible. The precision required here comes at an extra cost in terms of memory use and processing speed. However in some situations, precision is more important than speed.

## Example

None.

