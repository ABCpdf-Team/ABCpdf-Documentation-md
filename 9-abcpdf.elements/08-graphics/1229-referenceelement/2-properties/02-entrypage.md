---
title: "02-entrypage"
css: "abcpdf-docs.css"
---

# EntryPage Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "Page" entry of the reference dictionary object. | 

## Notes

Represents the "Page" entry of the reference dictionary object.

It is a required entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) An integer representing a PDF numeric object.

2) A string representing a PDF string object.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 97, page 221.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=229)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 95, page 272.](https://www.iso.org/standard/63534.md)

## Example

None.