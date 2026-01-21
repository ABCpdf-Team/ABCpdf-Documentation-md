---
title: "02-entryocgs"
css: "abcpdf-docs.css"
---

# EntryOCGs Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp ArrayElementOptionalContentGroupElement> ``` [Visual Basic] `ArrayElementOptionalContentGroupElement>` | null | No | Represents the "OCGs" entry of the optional content membership dictionary object. | 

## Notes

Represents the "OCGs" entry of the optional content membership dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains an array which contains [OptionalContentGroupElements](../../1230-optionalcontentgroupelement/default.md).

If you read the specification you will see that an array of one [OptionalContentGroupElement](../../1230-optionalcontentgroupelement/default.md) may be represented as a single [OptionalContentGroupElement](../../1230-optionalcontentgroupelement/default.md) rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 99, page 223.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=231)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 97, page 275.](https://www.iso.org/standard/63534.md)

## Example

None.