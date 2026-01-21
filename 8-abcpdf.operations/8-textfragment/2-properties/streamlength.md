---
title: "streamlength"
css: "abcpdf-docs.css"
---

# StreamLength Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | n/a | Yes | The length within the content stream of the drawing operation that contains this fragment. | 

## Notes

The length within the content stream of the drawing operation that contains this fragment.

Each TextFragment spans a part of a PDF stream drawing operator. This property provides the length from the offset within the uncompressed stream, to the end of that drawing operator.

## Example

None.