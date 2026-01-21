---
title: "gettagids"
css: "abcpdf-docs.css"
---

# GetTagIDs Function

Gets an array of the HTML IDs of tagged visible items.

## Syntax

**[C#]**

```csharp
string[] GetTagIDs(int id)
```

<span class=language>[Visual
            Basic]</span>  
`Function GetTagIDs(id As Integer) As String()`
## Params

| Name | Description | 
| --- | --- |
| id | The Object ID of the object. | 
| return | The IDs of tagged visible HTML objects. | 

## Notes

Use this method to retrieve the HTML IDs of tagged visible items.

To use this method you need to enable the tagging functionality. See the [AddTags](../2-properties/addtags.md) property for details.

This function takes an ID obtained from a call to [Doc.AddImageUrl,](../../doc/1-methods/addimageurl.md)[Doc.AddImageHtml](../../doc/1-methods/addimagehtml.md) or [Doc.AddImageToChain](../../doc/1-methods/addimagetochain.md) and returns the IDs of any items which are visible on the PDF page as a result of that call.

For example the ID associated with the following paragraph is "p1".

```html
Gallia est omnis divisa in partes tres.
```

The IDs may be repeated if the objects are split over more than one area.

The IDs match up directly on a one-to-one basis with the [XRects](../../xrect/default.md) returned by the [GetTagRects](gettagrects.md) or the [GetTagUntransformedRects](gettaguntransformedrects.md) function.

## Example

See the [GetTagRects](gettagrects.md) method.