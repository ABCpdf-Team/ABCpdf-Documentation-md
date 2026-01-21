# EntryTransferFunction Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "TransferFunction" entry of the type 1 halftone dictionary object. | 

## Notes

Represents the "TransferFunction" entry of the type 1 halftone dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) A string representing a PDF name object.

If provided, this item must always take the value "Identity".

2) A [FunctionElement](../../../07-syntax/1101-functionelement/default.md).

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 130, page 310.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=318)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 128, page 371.](https://www.iso.org/standard/63534.md)

## Example

None.