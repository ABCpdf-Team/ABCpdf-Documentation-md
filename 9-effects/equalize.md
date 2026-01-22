# Equalize Effect

## Settings

## Workings

Most images span an entire range of brightness with all levels well represented. However sometimes images are too light or too dark and some levels are overpopulated leaving others underpopulated.

The Equalize effect modifies an image so that all levels of brightness are equally well represented within the image.

## Example

The following example images show the effect of Equalize.

[C#] void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img2); // original image doc.Rendering.Save("EffectEqualize1.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Equalize")) { effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectEqualizeAfter1.jpg"); AddImagePage(doc, img6); // original image doc.Rendering.Save("EffectEqualize2.jpg"); using (ImageLayer layer = AddImagePage(doc, img6)) { using (EffectOperation effect = new EffectOperation("Equalize")) { effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectEqualizeAfter2.jpg"); } } [Visual Basic] Sub ... Using doc As New Doc() AddImagePage(doc, img2) ' original image doc.Rendering.Save("EffectEqualize1.jpg") Using layer As ImageLayer = AddImagePage(doc, img2) Using effect As New EffectOperation("Equalize") effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectEqualizeAfter1.jpg") AddImagePage(doc, img6) ' original image doc.Rendering.Save("EffectEqualize2.jpg") Using layer As ImageLayer = AddImagePage(doc, img6) Using effect As New EffectOperation("Equalize") effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectEqualizeAfter2.jpg") End Using End Sub

Original Image

After Equalize

Original Image

After Equalize

