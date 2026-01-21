---
title: "01-entryhalftonename"
css: "abcpdf-docs.css"
---

# EntryHalftoneName Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp string ``` [Visual Basic] `string` | null | No | Represents the "HalftoneName" entry of the type 6 halftone dictionary object. | 

## Notes

Represents the "HalftoneName" entry of the type 6 halftone dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains a string representing a PDF string object.

This string contains raw byte data. So it looks like a string but really it is just a wrapper for data.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 131, page 310.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=318)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 129, page 372.](https://www.iso.org/standard/63534.md)

## Example

None.