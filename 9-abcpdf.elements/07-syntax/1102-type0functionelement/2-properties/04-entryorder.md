---
title: "04-entryorder"
css: "abcpdf-docs.css"
---

# EntryOrder Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp int? ``` [Visual Basic] `Integer?` | null | No | Represents the "Order" entry of the type 0 function dictionary object. | 

## Notes

Represents the "Order" entry of the type 0 function dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains an integer representing a PDF numeric object.

It should have a minimum value of 1 and a maximum of 3.

The PDF specification states that this item assumes a value of 1 if no value has been provided.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 39, page 94.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=102)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 39, page 124.](https://www.iso.org/standard/63534.md)

## Example

None.