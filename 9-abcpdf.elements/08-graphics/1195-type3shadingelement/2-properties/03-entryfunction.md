---
title: "03-entryfunction"
css: "abcpdf-docs.css"
---

# EntryFunction Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp ArrayElementFunctionElement> ``` [Visual Basic] `ArrayElementFunctionElement>` | null | No | Represents the "Function" entry of the type 3 shading dictionary object. | 

## Notes

Represents the "Function" entry of the type 3 shading dictionary object.

It is a required entry defined as part of the PDF 1.0 specification.

It contains an array which contains [FunctionElements](../../../07-syntax/1101-functionelement/default.md).

If you read the specification you will see that an array of one [FunctionElement](../../../07-syntax/1101-functionelement/default.md) may be represented as a single [FunctionElement](../../../07-syntax/1101-functionelement/default.md) rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 81, page 187.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=195)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 80, page 233.](https://www.iso.org/standard/63534.md)

## Example

None.