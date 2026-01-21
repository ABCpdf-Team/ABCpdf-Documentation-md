---
title: "03-entrygamma"
css: "abcpdf-docs.css"
---

# EntryGamma Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp double? ``` [Visual Basic] `Double?` | null | No | Represents the "Gamma" entry of the calgray colour space dictionary object. | 

## Notes

Represents the "Gamma" entry of the calgray colour space dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains a double representing a PDF numeric object.

It should have a positive value.

The PDF specification states that this item assumes a value of 1 if no value has been provided.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 63, page 145.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=153)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 62, page 183.](https://www.iso.org/standard/63534.md)

## Example

None.