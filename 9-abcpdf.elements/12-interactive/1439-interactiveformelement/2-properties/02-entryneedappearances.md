---
title: "02-entryneedappearances"
css: "abcpdf-docs.css"
---

# EntryNeedAppearances Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool? ``` [Visual Basic] `Boolean?` | null | No | Represents the "NeedAppearances" entry of the interactive form dictionary object. | 

## Notes

Represents the "NeedAppearances" entry of the interactive form dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification. It was deprecated in PDF 2.0.

It contains a bool representing a PDF boolean object.

The PDF specification states that this item assumes a value of false if no value has been provided.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 218, page 431.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=439)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 224, page 525.](https://www.iso.org/standard/63534.md)

## Example

None.