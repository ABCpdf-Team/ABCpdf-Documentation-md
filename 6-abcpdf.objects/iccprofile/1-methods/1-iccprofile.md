# IccProfile Constructor

IccProfile Constructor.

## Syntax

**[C#]**

```csharp
IccProfile(ObjectSoup soup, byte[] data)
IccProfile(ObjectSoup soup, string path)
```

**[Visual Basic]**

```
Sub New(soup As ObjectSoup, data() As Byte)
Sub New(soup As ObjectSoup, path As String)
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created IccProfile. | 
| data | An ICC profile stored in an array of bytes. | 
| path | A path to an ICC file. | 

## Notes

Create an IccProfile object.

If the content provided is not a valid ICC profile then an exception will be thrown.

## Example

See the [PixMap.Recolor](../../pixmap/1-methods/recolor.md) function.