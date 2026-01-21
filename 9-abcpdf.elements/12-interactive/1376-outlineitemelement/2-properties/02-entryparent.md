---
title: "02-entryparent"
css: "abcpdf-docs.css"
---

# EntryParent Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "Parent" entry of the outline item dictionary object. | 

## Notes

Represents the "Parent" entry of the outline item dictionary object.

It is a required entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) An [OutlineElement](../../1376-outlineelement/default.md).

2) An [OutlineItemElement](../default.md).

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 153, page 368.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=376)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 151, page 442.](https://www.iso.org/standard/63534.md)

## Example

None.