# EncodeDoubleByte  Function

## Syntax

[C#] static StringBuilder EncodeDoubleByte(string text, IDictionary<char, char> encoding, StringBuilder builder)

## Params

## Notes

Encode a string into a format for use in a content stream using a composite font with a double byte CMap.

Typically you will obtain an appropriate encoding from the FontObject.GetEncoding method. This method supports eight bit characters only as this is what is supported by simple fonts. Most commonly you will want to use a Korean, Japanese, ChineseS or ChineseT encoding in either horizontal or vertical format.

This method should only be used with composite fonts that specify this type of encoding as only these fonts will understand the fact that the characters are multi-byte. If you attempt to use this method with a simple font then you will get extra characters inserted since each double byte entry will be interpreted as two single characters.

See the Fonts and Languages section for details on language types.

## Example

None.

