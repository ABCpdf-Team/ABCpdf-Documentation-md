# IccProfile Constructor

## Syntax

[C#] IccProfile(ObjectSoup soup, byte[] data) IccProfile(ObjectSoup soup, string path) [Visual Basic] Sub New(soup As ObjectSoup, data() As Byte) Sub New(soup As ObjectSoup, path As String)

may throw Exception()

## Params

## Notes

Create an IccProfile object.

If the content provided is not a valid ICC profile then an exception will be thrown.

## Example

See the PixMap.Recolor function.

