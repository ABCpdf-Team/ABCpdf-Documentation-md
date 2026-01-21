---
title: "02-entrytf"
css: "abcpdf-docs.css"
---

# EntryTF Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp string ``` [Visual Basic] `string` | null | No | Represents the "TF" entry of the media permissions dictionary object. | 

## Notes

Represents the "TF" entry of the media permissions dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains a string representing a PDF string object.

This is encoded as a string using single byte ASCII encoding.

The PDF specification states that this item assumes a value of "TEMPNEVER" if no value has been provided.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 275, page 494.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=502)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 286, page 619.](https://www.iso.org/standard/63534.md)

## Example

None.