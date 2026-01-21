---
title: "embeddedfile"
css: "abcpdf-docs.css"
---

# EmbeddedFile Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp EmbeddedFile ``` [Visual Basic] `EmbeddedFile` | null | No | The embedded file if one has been embedded in the PDF | 

## Notes

The embedded file if one has been embedded in the PDF.

If a file has not been embedded then the URL needs to be intepreted in the context of the current PDF to locate the external file.

Setting this property will clear the EmbeddedFiles property if one is present.

This property requires reference to other objects in the ObjectSoup. If this object is not part of an ObjectSoup this property will always be null.

## Example

Also see example code in: [FileSpecification FileSpecification Function](../1-methods/filespecification.md).