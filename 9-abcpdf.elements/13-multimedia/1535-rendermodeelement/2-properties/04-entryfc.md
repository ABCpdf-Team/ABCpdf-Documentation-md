# EntryFC Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "FC" entry of the render mode dictionary object. | 

## Notes

Represents the "FC" entry of the render mode dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) A string representing a PDF name object.

The PDF specification states that this item assumes a value of "BG" if no value has been provided.

If provided, this item must always take the value "BG".

2) An array which contains [Elements](../../../01-base/1086-element/default.md).

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 307, page 528.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=536)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 318, page 660.](https://www.iso.org/standard/63534.md)

## Example

None.