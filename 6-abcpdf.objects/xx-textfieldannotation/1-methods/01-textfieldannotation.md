---
title: "01-textfieldannotation"
css: "abcpdf-docs.css"
---

# TextFieldAnnotation Function

Add textfield annotation to the current page of the doc.

## Syntax

**[C#]**

```csharp
TextFieldAnnotation(Doc doc, XRect rect)
```

<span class=language>[Visual Basic]</span>  

            `TextFieldAnnotation(doc As Doc, rect As XRect)`
			
## Params

| Name | Description | 
| --- | --- |
| doc | Doc | 
| rect | Location for the annotation | 

## Notes

Add textfield annotation to the current page of the doc.

Note that the annotation created using this constructor is meaningless until it is connected with a [Field](../../field/default.md). For this reason you are likely to want to use [Doc.Form.AddTextField](../../../5-abcpdf/xform/1-methods/addtextfield.md) rather than this call.

## Example

None.