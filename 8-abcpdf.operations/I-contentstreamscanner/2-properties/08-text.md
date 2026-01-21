---
title: "08-text"
css: "abcpdf-docs.css"
---

# Text Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp TextState ``` [Visual Basic] `TextState` | null | Yes | The current text state. | 

## Notes

The current text state. Text state is not saved and restored using the PDF save and restore operators.

Text state operators can occur anywhere in a content stream but typically they only occur within text blocks.

A text block initializes a text matrix which allows text positioning and text showing. At the end of the text block the matrix is discarded.

## Example

None.