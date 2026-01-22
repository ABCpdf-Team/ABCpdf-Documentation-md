# SetChromakey Function

## Syntax

[C#] void SetChromakey(string chromakey) [Visual Basic] Sub SetChromakey(chromakey As String)

## Params

## Notes

This allows you to assign a transparent color or color range to the image.

You need to specify two values for each component of the color. For a particular pixel, if all the components of the color fall within the specified ranges, then the pixel will not be displayed.

For example, to make pure white elements of an RGB transparent you might specify,

[C#] doc.SetChromakey("255 255 255 255 255 255"); [Visual Basic] doc.SetChromakey("255 255 255 255 255 255")

If you wanted to include colors which were off-white you might use,

[C#] doc.SetChromakey("250 255 250 255 250 255"); [Visual Basic] doc.SetChromakey("250 255 250 255 250 255")

This function is equivalent to setting the PixMap "/Mask" entry to an array of color values.

## Example

Here we add an image over the top of a green background. We use a chromakey to make black and near-black colors transparent.

[C#] using var doc = new Doc(); doc.Rect.Inset(20, 20); doc.Color.String = "0 255 0"; doc.FillRect(); string path = Server.MapPath("../mypics/mypic.jpg"); int i = doc.AddImageFile(path, 1); var im = (ImageLayer)doc.ObjectSoup[i]; im.PixMap.SetChromakey("0 50 0 50 0 50"); doc.Save(Server.MapPath("pixmapsetchromakey.pdf")); [Visual Basic] Using doc As New Doc() doc.Rect.Inset(20, 20) doc.Color.String = "0 255 0" doc.FillRect() Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") Dim i As Integer = doc.AddImageFile(thePath, 1) Dim im As ImageLayer = DirectCast(doc.ObjectSoup(i), ImageLayer) im.PixMap.SetChromakey("0 50 0 50 0 50") doc.Save(Server.MapPath("pixmapsetchromakey.pdf")) End Using

pixmapsetchromakey.pdf

