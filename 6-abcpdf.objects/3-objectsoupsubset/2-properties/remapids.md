---
title: "remapids"
css: "abcpdf-docs.css"
---

# RemapIDs Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IDictionary ``` [Visual Basic] `IDictionary` | n/a | Yes | Gets the dictionary used to map object IDs from the source soup to new object IDs in the final soup. | 

## Notes

Gets the dictionary used to map object IDs from the source soup to new object IDs in the final soup.

Some mappings may be populated via the [RemapTypes](remaptypes.md) as [IndirectObjects](../../1-indirectobject/default.md) are added. Most will be populated at the point that the [CopyTo](../1-methods/2-copyto.md) method is called.

## Example

None.