# AddLayers Function

Add a particular set of Layer objects from a particular Page

## Syntax

[C#]

```csharp
void AddLayers(<a href="../../../6-abcpdf.objects/page/default.htm">Page</a> page, <a href="../../../6-abcpdf.objects/layer/default.htm">Layer</a>[] layers)
```

[Visual Basic]

```vb
Sub AddLayers(page As <a href="../../../6-abcpdf.objects/page/default.htm">Page</a>, layers() As <a href="../../../6-abcpdf.objects/layer/default.htm">Layer</a>)
```

## Params

| **Name** | **Description** |
| --- | --- |
| page | The page on which the provided layers are located. |
| layers | The layers to be added. |

## Notes

Add a particular set of Layer objects from a particular Page.

This is an alternative to the [AddPages](addpages.md) overloads. It allows specific parts of a page to be added to the operation rather than requiring the operation to be applied to the entirety of a page.

## Example

None
