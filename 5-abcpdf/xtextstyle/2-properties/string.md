---
title: "string"
css: "abcpdf-docs.css"
---

# String Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp string ``` [Visual Basic]`String` | Variable | No | The text style as a string. | 

## Notes

A string representation of the text style.

This covers all the properties of this class and can be sued for a save and restore stack.

## Example

The following code.

[C#]

```csharp
var ts = new XTextStyle();
ts.String = "24.5 10 0 0 0 0 0";
Response.Write($"Size = {ts.Size}&lt;br&gt;");
Response.Write($"Indent = {ts.Indent}");
```

<span class=language>[Visual
            Basic]</span>
```vbnet
Dim ts As New XTextStyle()
ts.String = "24.5 10 0 0 0 0 0"
Response.Write($"Size = {ts.Size}&lt;br&gt;")
Response.Write($"Indent = {ts.Indent}")
```

Produces the following output.

Size = 24.5Indent = 10