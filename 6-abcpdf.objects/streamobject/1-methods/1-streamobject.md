# StreamObject Constructor

## Syntax

[C#] StreamObject(ObjectSoup soup) StreamObject(ObjectSoup soup, byte[] data) StreamObject(ObjectSoup soup, string path) [Visual Basic] Sub New(soup As ObjectSoup) Sub New(soup As ObjectSoup, data() As Byte) Sub New(soup As ObjectSoup, path As String)

may throw Exception()

## Params

## Notes

Create a StreamObject.

If no arguments are passed then the StreamObject contains no data. No exception will be thrown.

If an array of bytes is passed then the StreamObject data will be initialized with the contents of the array. No exception will be thrown.

If a string is passed then the StreamObject data will be initialized with the contents of the file. If the file cannot be read then an exception is thrown.

## Example

None.

