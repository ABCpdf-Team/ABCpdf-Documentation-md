---
title: "autotruncate"
css: "abcpdf-docs.css"
---

# AutoTruncate Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to automatically clip redundant content at the end of the page. | 

## Notes

This property determines whether redundant content at the end of an HTML page is shown or not.

Redundancy is determined using a number of heuristics. However most commonly it covers repeating background images which do not need to be shown.

## Example

None.