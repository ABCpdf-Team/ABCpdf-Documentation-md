# PDF Rendering Example

## Read

We create an ABCpdf Doc object and read our source PDF.

[C#] using Doc doc = new Doc(); doc.Read("../Rez/spaceshuttle.pdf");

## Prefs

We specify our base rendering settings.

[C#] doc.Rendering.DotsPerInch = 36;

## Save

Finally we save the first four pages of the document in png format.

[C#] for (int i = 1; i <= 4; i++) { doc.PageNumber = i; doc.Rect.String = doc.CropBox.String; doc.Rendering.Save("shuttle_p" + i.ToString() + ".png"); }

## Results

shuttle_p1.png

shuttle_p2.png

shuttle_p3.png

shuttle_p4.png

