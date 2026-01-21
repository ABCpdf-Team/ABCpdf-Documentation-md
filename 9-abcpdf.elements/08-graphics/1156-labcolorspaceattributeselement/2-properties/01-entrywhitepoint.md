---
title: "01-entrywhitepoint"
css: "abcpdf-docs.css"
---

# EntryWhitePoint Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | Represents the "WhitePoint" entry of the lab colour space dictionary object. | 

## Notes

Represents the "WhitePoint" entry of the lab colour space dictionary object.

It is a required entry defined as part of the PDF 1.0 specification.

It contains an array which contains doubles, representing PDF numeric objects.

Items in this array should have a positive value.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 65, page 148.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=156)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 64, page 186.](https://www.iso.org/standard/63534.md)

## Example

None.