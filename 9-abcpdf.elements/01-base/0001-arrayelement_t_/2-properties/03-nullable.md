---
title: "03-nullable"
css: "abcpdf-docs.css"
---

# Nullable Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether NullAtom values are acceptable within the array. | 

## Notes

Whether NullAtom values are acceptable within the array.

In most cases null values are not appropriate within an [ArrayElement](../default.md).

In occasional cases it is possible to represent missing elements using a NullAtom.

This property allows you to determine if this should be the case.

## Example

None.