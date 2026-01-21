---
title: "05-roottag"
css: "abcpdf-docs.css"
---

# RootTag Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IndirectObject ``` [Visual Basic] `IndirectObject` | null | No | The root structure element for the added tags. | 

## Notes

The root structure element for the added tags.

When [CopyTags](/8-abcpdf.operations/F-drawpagesoperation/2-properties/04-copytags.md) is set to true, the tags for the source page are grouped under one tag before copying to the destination document.

The group is inserted as the last item on the destination page but depending on your document semantics you may wish to adjust this.

This property holds the last group added as a result of calling [DrawPage](/8-abcpdf.operations/F-drawpagesoperation/1-methods/02-drawpage.md).

## Example

None.