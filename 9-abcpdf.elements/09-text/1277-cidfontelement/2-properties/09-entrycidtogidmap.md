# EntryCIDToGIDMap Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "CIDToGIDMap" entry of the cidfont dictionary object. | 

## Notes

Represents the "CIDToGIDMap" entry of the cidfont dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) A string representing a PDF name object.

The PDF specification states that this item assumes a value of "Identity" if no value has been provided.

If provided, this item must always take the value "Identity".

2) A [StreamElement](../../../07-syntax/1028-streamelement/default.md).

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 117, page 270.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=278)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 115, page 327.](https://www.iso.org/standard/63534.md)

## Example

None.