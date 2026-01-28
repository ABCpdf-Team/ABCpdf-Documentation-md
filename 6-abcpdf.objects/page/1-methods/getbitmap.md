# GetBitmap Function

Render one or more layers on the current page

## Syntax

[C#]

```csharp
System.Drawing.Bitmap GetBitmap(Layer[] layers)
```

## Params

| **Name** | **Description** |
| --- | --- |
| layers | The layers to be rendered. |
| return | The System.Drawing.Bitmap containing the image of the layers. |

## Notes

Render one or more layers on the current page.

This function renders a set of layers and returns the result as a System.Drawing.Bitmap. The Bitmap covers the smallest possible area which encompasses all the layers provided.

If this Page is not in a Doc then an exception will be raised. The function will return null if the layers argument is null or empty or the output Bitmap would be smaller than one pixel in area.

Rendering options such as resolution are taken directly from the current [Doc.Rendering](5-abcpdf/doc/2-properties/rendering.md) settings. However automatic page rotation (XRendering.AutoRotate) is disabled so that a Layer can be rendered and then re-inserted into the page as a raster copy of itself.

Note that a layer can exist on multiple pages and indeed can be rendered in the context of a page that does not currently contain it. However layers typically contain references to named resources which are only available in the context of a specific page. So rendering a layer in the context of a page which does not normally contain it is prone to error unless the page and layer have been specifically constructed to allow this.

## Example

[C#]

```csharp
using var doc = new Doc();
// light blue background
doc.Color.SetCmyk(50, 0, 0, 0);
doc.FillRect();
doc.Color.SetRgb(0, 0, 0);
doc.Rect.Inset(20, 20);
doc.Rect.Pin = XRect.Corner.TopLeft;
doc.Rect.Height = doc.Rect.Height / 5;
// set up styles
doc.TextStyle.Size = 72;
double shift = doc.TextStyle.Size * 0.1;
var pink = new XColor();
pink.SetRgb(255, 128, 128);
var gray = new XColor();
gray.SetRgb(128, 128, 128);
var blue = new XColor();
blue.SetRgb(0, 0, 255);
// add text content
AddDropShadow(doc, doc.AddText("Sharp Shadow"), 0, shift, -shift, gray);
doc.Rect.Move(0, -doc.Rect.Height);
AddDropShadow(doc, doc.AddText("Blurred Shadow"), 1, shift, -shift, gray);
doc.Rect.Move(0, -doc.Rect.Height);
AddDropShadow(doc, doc.AddText("Pink Shadow"), 1, shift, -shift, pink);
doc.Rect.Move(0, -doc.Rect.Height);
// add drawn content
doc.Transform.Magnify(0.5, 0.5, 0, 0);
doc.Transform.Translate(50, 0);
string star = "124 158 300 700 476 158 15 493 585 493 124 158";
doc.Width = 20;
doc.Color.String = "255 0 0";
AddDropShadow(doc, doc.AddPoly(star, false), 3, shift, -shift, blue);
doc.Save("dropshadows.pdf");
```

![](../../../images/pdf/dropshadows.pdf.png)
dropshadows.pdf

