# CheckBoxAnnotation Function

Add checkbox annotation to the current page of the doc.

## Syntax

[C#]

```csharp
<a href="../default.htm">CheckBoxAnnotation</a>(Doc doc, XRect rect, bool selected)
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | Doc |
| rect | Location for the annotation |
| selected | Whether the checkbox should be checked or not |

## Notes

Add checkbox annotation to the current page of the doc.

Note that the annotation created using this constructor is meaningless until it is connected with a [Field](field/default.md). For this reason you are likely to want to use [Doc.Form.AddCheckbox](5-abcpdf/xform/1-methods/addcheckbox.md) rather than this call.

## Example

None
