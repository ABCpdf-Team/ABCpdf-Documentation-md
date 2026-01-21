---
title: "01-widgetannotation"
css: "abcpdf-docs.css"
---

# WidgetAnnotation Function

Add widget annotation to the doc.

## Syntax

**[C#]**

```csharp
WidgetAnnotation(Doc doc)
```

<span class=language>[Visual Basic]</span>  

            `WidgetAnnotation(doc As Doc)`
			
## Params

| Name | Description | 
| --- | --- |
| doc | Doc | 

## Notes

Add widget annotation to the doc.

Note that the annotation created using this constructor is meaningless until it is connected with a [Field](../../field/default.md). For this reason you are likely to want to use methods such as [Doc.Form.AddCheckbox](../../../5-abcpdf/xform/1-methods/addcheckbox.md) rather than these types of call.

## Example

None.