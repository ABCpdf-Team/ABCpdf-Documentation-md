---
title: "05-entrykeyusage"
css: "abcpdf-docs.css"
---

# EntryKeyUsage Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | Represents the "KeyUsage" entry of the certificate seed value dictionary object. | 

## Notes

Represents the "KeyUsage" entry of the certificate seed value dictionary object.

It is an optional entry defined as part of the PDF 1.7 specification.

It contains an array which contains strings, representing PDF string objects.

This is encoded as a string using single byte ASCII encoding.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 235, page 450.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=458)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 238, page 546.](https://www.iso.org/standard/63534.md)

## Example

None.