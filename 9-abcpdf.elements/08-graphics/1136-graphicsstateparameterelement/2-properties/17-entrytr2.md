# EntryTR2 Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "TR2" entry of the graphics state parameter dictionary object. | 

## Notes

Represents the "TR2" entry of the graphics state parameter dictionary object.

It is an optional entry defined as part of the PDF 1.3 specification. It was deprecated in PDF 2.0.

This property may contain one of two different types:.

1) A string representing a PDF name object.

This item may take one of the following valid values:.

- Identity
- Default

.2) An array which contains [FunctionElements](../../../07-syntax/1101-functionelement/default.md).

If you read the specification you will see that an array of one [FunctionElement](../../../07-syntax/1101-functionelement/default.md) may be represented as a single [FunctionElement](../../../07-syntax/1101-functionelement/default.md) rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 58, page 129.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=137)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 57, page 163.](https://www.iso.org/standard/63534.md)

## Example

None.