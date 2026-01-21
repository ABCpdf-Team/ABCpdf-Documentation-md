---
title: "01-entrytarget"
css: "abcpdf-docs.css"
---

# EntryTarget Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | This property represents the destination target. | 

## Notes

This property represents the destination target.

It is a required entry and defined as part of the PDF 1.0 specification.

The Target may be a [PageObjectElement](../../1085-pageobjectelement/default.md) or, in the case of a remote destination, an [Element](../../../01-base/1086-element/default.md) containing a NumAtom indicating a page number. In this case page numbers use a zero rather than one based index.

In a PDF 2.0 document this property may be a [StructureElementElement](../../../14-document/1566-structureelementelement/default.md) indicating the part of the document to which the destination refers.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 151, page 366.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=374)

## Example

None.