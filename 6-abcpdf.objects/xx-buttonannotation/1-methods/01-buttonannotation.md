# ButtonAnnotation Function

Add button annotation to the current page of the doc.

## Syntax

**[C#]**

```csharp
ButtonAnnotation(Doc doc, XRect rect, string caption)
```

<span class=language>[Visual Basic]</span>  

            `ButtonAnnotation(doc As Doc, rect As XRect, caption As string)`
			
## Params

| Name | Description | 
| --- | --- |
| doc | Doc | 
| rect | Location for the annotation | 
| caption | Caption for button | 

## Notes

Add button annotation to the current page of the doc.

Note that the annotation created using this constructor is meaningless until it is connected with a [Field](../../field/default.md). For this reason you are likely to want to use [Doc.Form.AddButton](../../../5-abcpdf/xform/1-methods/addbutton.md) rather than this call.

## Example

None.