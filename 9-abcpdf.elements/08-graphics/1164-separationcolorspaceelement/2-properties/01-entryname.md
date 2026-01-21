# EntryName Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp string ``` [Visual Basic] `string` | null | No | This property represents the name of the separation color space. | 

## Notes

This property represents the name of the separation color space.

The name is an arbitrary value such as "Flame" which intended for human readability.

It may also take the special values "All" or "None".

The former means all available colorants on an output device while the latter means none of them.

As such the value "All" will typically output rich black and the latter will output nothing.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 157.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=165)

## Example

None.