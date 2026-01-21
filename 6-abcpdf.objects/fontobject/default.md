---
title: "default"
css: "abcpdf-docs.css"
---

# FontObject Class

A specific font as used in the document.

``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.FontObject ```

## Method Description S&raquo;&nbsp; &nbsp;GetEncoding Obtain a standard encoding dictionary for use with PDF text operators. S&raquo;&nbsp; &nbsp;VetText Make a string of text safe for use in a specified encoding. EmbedFont Search for and embed a font file into this font object. &nbsp;EncodeText Encode text for use with PDF text operators. GetVerticalMetric Get the vertical metric for a character. RegenerateToUnicode Attempt to regenerate a ToUnicode map. Subset Subset a previously embedded font. UnembedSimpleFont Unembed the font if this is a simple operation. &nbsp;

## Property Description BaseFont The PostScript name of the font. EmbeddedFont The embedded font file. IsComposite Whether the font is a complex composite font. IsIdentity Whether the font is a composite glyph encoded identity font. IsSubset Whether the font contains an embedded subset. IsVertical Whether the font is for vertical writing. WritingMode Gets the font writing mode. Widths The widths of the characters in the font. CharToEncoding The Unicode to glyph mapping table for all the characters in the font. CheckGlyphs Whether to exclude invalid glyphs from our lookup tables. DefaultWidth The default character width. EncodingToChar The glyph to Unicode mapping table for all the characters in the font. EncodingToString The glyph to Unicode string mapping table. Flags The Font Descriptor Flags entry. FontAscender The ascender for the glyphs in this font. FontAscent The ascent for the glyphs in this font. FontBBox The bounding box for the glyphs in this font. FontDescender The descender for the glyphs in this font. FontDescent The descent for the glyphs in this font. FontLineGap The line gap for the glyphs in this font. FontLineSpacing The line spacing for the glyphs in this font. IsDescendent Whether the font is a descendent of a complex composite font. NativeWidths The character widths indexed by native character code.