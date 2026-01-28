# Encode Function

## Syntax

[C#] static StringBuilder Encode(string text, IDictionary<char, char> encoding, StringBuilder builder)

## Params

## Notes

Encode a string into a format for use in a content stream using a normal or simple font.

Typically you will obtain an appropriate encoding from the FontObject.GetEncoding method. This method supports eight bit characters only as this is what is supported by simple fonts. Most commonly you will want to use the Latin horizontal encoding.

You should not use a null or identity encoding as there are subtle differences between the Latin1 encoding used in PDF and the first 256 characters of Unicode. As such if you use a null or identity encoding then characters such as the Euro sign will appear incorrectly.

## Example

None.

