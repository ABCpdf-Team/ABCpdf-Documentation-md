---
title: "08-entryencoding"
css: "abcpdf-docs.css"
---

# EntryEncoding Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "Encoding" entry of the type 1 font dictionary object. | 

## Notes

Represents the "Encoding" entry of the type 1 font dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) A string representing a PDF name object.

This item may take one of the following valid values:.

- MacRomanEncoding
- MacExpertEncoding
- WinAnsiEncoding

.2) An [EncodingElement](../../1271-encodingelement/default.md).

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 111, page 255.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=263)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 109, page 311.](https://www.iso.org/standard/63534.md)

## Example

None.