# CheckGlyphs Property

## Notes

Whether to exclude invalid glyphs from our lookup tables.

When fonts are subsetted the glyphs in the tables may be rendered invalid because they are not used. The encoding continues to exist but the information required to draw the glyphs has been lost. As such it is not a good idea to attempt to use these glyphs even though they may appear to be part of the font.

By default we attempt to detect such glyphs and exclude them from any operations or font properties such as the EncodingToChar and CharToEncoding mappings. This prevents them being used inadvertently.

## Example

None.

