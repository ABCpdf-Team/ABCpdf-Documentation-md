# Flatten Function

Flattens and compresses the current page.

## Syntax

[C#]

```csharp
int Flatten()
```

## Params

| **Name** | **Description** |
| --- | --- |
| return | n/a. |

## Notes

Objects added to a page are stored as individual layers. Calling this method combines all the layers on the current page and then re-compresses the layer data.

For pages that contain only a few layers the reduction in size will be minimal. However for pages which contain complex tables with many items, flattening can reduce the size of the output PDF by a factor of five or more.

Note that flattening will delete all the items currently on the page and replace them with a new compressed item. This means that Object IDs previously obtained from calls such as [AddText](addtext.md) or [FrameRect](framerect.md) will no longer be valid.

## Example

Also see example code in:

* [ABCpdf Small Table Example](4-examples/09-table1.md)
* [ABCpdf Large Table Example](4-examples/10-table2.md)
* [ABCpdf Paged HTML Example](4-examples/13-pagedhtml.md)
* [Doc AddImageToChain Function](addimagetochain.md)
* [XHtmlOptions LinkDestinations Method](xhtmloptions/1-methods/linkdestinations.md)
* [XHtmlOptions LinkPages Method](xhtmloptions/1-methods/linkpages.md)
* [XHtmlOptions UseScript Property](xhtmloptions/2-properties/usescript.md).
