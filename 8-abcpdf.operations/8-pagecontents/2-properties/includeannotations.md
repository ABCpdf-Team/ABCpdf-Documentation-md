---
title: "includeannotations"
css: "abcpdf-docs.css"
---

# IncludeAnnotations Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to include annotation and field text in the output. | 

`may throw Exception()`

## Notes

Whether to include annotation and field text in the output.

This property must not be changed after the [AddPages](../1-methods/addpages.md) method has been called. To do so will result in an exception being raised.

## Example

None.