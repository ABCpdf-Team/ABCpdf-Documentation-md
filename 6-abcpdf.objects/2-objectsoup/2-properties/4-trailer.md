---
title: "4-trailer"
css: "abcpdf-docs.css"
---

# Trailer Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp StreamObject ``` [Visual Basic] `StreamObject` | n/a | Yes | The Trailer or XRef for the document. | 

## Notes

The Trailer or XRef [StreamObject](../../streamobject/default.md) for the document.

In PDF 1.4 documents have trailer dictionary. In PDF 1.5 documents have XRef streams. Internally ABCpdf only uses XRef streams but - when writing PDF 1.4 documents - it converts the XRef to a standard trailer before output.

## Example

None.