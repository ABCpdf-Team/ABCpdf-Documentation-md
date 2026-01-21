---
title: "03-entryrt"
css: "abcpdf-docs.css"
---

# EntryRT Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp int? ``` [Visual Basic] `Integer?` | null | No | Represents the "RT" entry of the floating window parameters dictionary object. | 

## Notes

Represents the "RT" entry of the floating window parameters dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains an integer representing a PDF numeric object.

The PDF specification states that this item assumes a value of 0 if no value has been provided.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 284, page 500.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=508)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 295, page 626.](https://www.iso.org/standard/63534.md)

## Example

None.