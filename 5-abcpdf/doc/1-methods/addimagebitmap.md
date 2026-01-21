# AddImageBitmap Function

Adds a System.Drawing.Bitmap to the current page.

## Syntax

**[C#]**

```csharp
int AddImageBitmap(System.Drawing.Bitmap bm, bool transparent)
```

<span class=language>[Visual
            Basic]</span>  
`Function AddImageBitmap(bm As System.Drawing.Bitmap, transparent As Boolean) As Integer``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| bm | A .NET Bitmap to be added to the page. | 
| transparent | Whether transparency information should be preserved. | 
| return | The ID of the newly added Image Object. | 

## Notes

Adds a System.Drawing.Bitmap to the current page.

If the Transparent parameter is set to true then any transparency information will be preserved. This allows you to add formats such as transparent GIF and PNG with alpha channel.

The image is scaled to fill the current [Rect](../2-properties/rect.md). It is transformed using the current [Transform](../../xtransform/default.md).

## Example

The following code adds a transparent PNG to a document.

[C#]

```csharp
using var doc = new Doc();
string path = Server.MapPath("../mypics/mypic.png");
using var bm = new Bitmap(path);
doc.Rect.Inset(20, 20);
doc.Color.String = "0 0 200";
doc.FillRect();
doc.AddImageBitmap(bm, true);
bm.Dispose();
doc.Save(Server.MapPath("docaddimagebitmap.pdf"));
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc()
  Dim thePath As String = Server.MapPath("../mypics/mypic.png")
  Dim bm As New Bitmap(thePath)
  doc.Rect.Inset(20, 20)
  doc.Color.String = "0 0 200"
  doc.FillRect()
  doc.AddImageBitmap(bm, True)
  bm.Dispose()
  doc.Save(Server.MapPath("docaddimagebitmap.pdf"))
End Using
```

![](../../../images/pdf/docaddimagebitmap.pdf.png)docaddimagebitmap.pdf

Also see example code in: [XRendering AntiAliasPolygons Property](../../xrendering/2-properties/antialiaspolygons.md), [XRendering AntiAliasText Property](../../xrendering/2-properties/antialiastext.md), [XRendering SaveAlpha Property](../../xrendering/2-properties/savealpha.md).