# SetAlpha Function

## Syntax

[C#] void SetAlpha(double alpha) [Visual Basic] Sub SetAlpha(alpha As Double)

## Params

## Notes

Assigns a constant alpha transparency to the PixMap.

The alpha value should range from 0 (fully transparent) to 255 (fully opaque). Any values outside this range will result in the alpha channel being removed.

## Example

Here we add an image without transparency and then, at a position down and to the right, with 50% transparency.

[C#] using var doc = new Doc(); doc.Rect.Pin = XRect.Corner.TopLeft; doc.Rect.Magnify(0.5, 0.5); string path = Server.MapPath("../mypics/mypic.jpg"); doc.AddImageFile(path, 1); doc.Rect.Move(doc.Rect.Width, -doc.Rect.Height); int i = doc.AddImageFile(path, 1); var im = (ImageLayer)doc.ObjectSoup[i]; im.PixMap.SetAlpha(128); doc.Save(Server.MapPath("pixmapsetalpha.pdf")); [Visual Basic] Using doc As New Doc() doc.Rect.Pin = XRect.Corner.TopLeft doc.Rect.Magnify(0.5, 0.5) Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") doc.AddImageFile(thePath, 1) doc.Rect.Move(doc.Rect.Width, -doc.Rect.Height) Dim i As Integer = doc.AddImageFile(thePath, 1) Dim im As ImageLayer = DirectCast(doc.ObjectSoup(i), ImageLayer) im.PixMap.SetAlpha(128) doc.Save(Server.MapPath("pixmapsetalpha.pdf")) End Using

pixmapsetalpha.pdf

