# VirtualPageOperation Function

## Syntax

[C#]

```csharp
<a href="../default.htm">VirtualPageOperation</a>(Doc doc)<a href="../default.htm">VirtualPageOperation</a>(Doc doc, double width, double height)<a href="../default.htm">VirtualPageOperation</a>(Doc doc, XRect rect)
```

[Visual Basic]

```vb
<a href="../default.htm">VirtualPageOperation</a>(doc As Doc)<a href="../default.htm">VirtualPageOperation</a>(doc As Doc, width As double, height As double)<a href="../default.htm">VirtualPageOperation</a>(doc As Doc, rect As XRect)
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | The Doc for which the page is intended. |
| width | The width of the page in points. |
| height | The height of the page in points. |
| rect | The rectangle for the page in points. |

## Notes

Create a [VirtualPageOperation](default.md).

If no page dimensions are specified the page will default to the current document MediaBox.

Creating this process sets the current Doc.Page to the newly created virtual page. This means you can immediately use Doc methods to add content to this page.

However it also means that after you have finished with this object, you will need to set the Doc.Page before you can add content to existing pages of the document.

## Example

None
