# AddImageToChain Function

Adds a new page from a paged HTML or PostScript render.

## Syntax

[C#]

```csharp
int AddImageToChain(int id)
```

[Visual Basic]

```vb
Function AddImageToChain(id As Integer) As Integer
```

## Params

| **Name** | **Description** |
| --- | --- |
| id | The ID of the previous object in the chain. |
| return | The ID of the newly added object. |

## Notes

Some web pages are too large to fit on one PDF page.

To split a web page across multiple PDF pages you need to call [AddImageUrl](addimageurl.md) or [AddImageHtml](addimageurl.md) to render the first page. The ID returned from these calls represents the head of the chain.

To add subsequent pages to the chain you need to make calls to AddImageToChain passing in the previous image from the chain each time.

As well as using chaining to split web pages across multiple PDF pages you can also use it to split your web pages across multiple columns within a page. You can even split your chain to generate multiple copies of the same page.

More information can be found in the [HTML / CSS Rendering](3-concepts/g-htmlrender.md) section of the documentation.

Similarly some PostScript (PS) files contain more than one page of content.

To split a PS file across multiple PDF pages you need to call [AddImageFile](addimagefile.md) or [AddImageData](addimagedata.md) to render the first page. The ID returned from these calls represents the head of the chain.

To add subsequent pages to the chain you need to make calls to AddImageToChain passing in the previous image from the chain each time.

## Example

This example shows how to import an HTML page into a multi-page PDF document. We first create a [Doc](default.md) object and inset the edges a little so that the HTML will appear in the middle of the page.

[C#]

```csharp
using var doc = new Doc();
doc.Rect.Inset(72, 144);
```

[Visual Basic]

```vb
Using doc As New Doc()
  doc.Rect.Inset(72, 144)
```

