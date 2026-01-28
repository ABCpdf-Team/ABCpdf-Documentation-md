# Contrast Effect

## Settings

Amount to increase or decrease contrast by.

## Workings

The value given is used to stretch the contrast within the image. Values greater than zero increase the amount of contrast while those less than zero decrease the contrast.

## Example

The following show the effect of increasing and decreasing contrast.

[C#] void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img2); // original image doc.Rendering.Save("EffectContrast.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Contrast")) { effect.Parameters["Amount"].Value = 25; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectContrast25.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Contrast")) { effect.Parameters["Amount"].Value = 50; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectContrast50.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Contrast")) { effect.Parameters["Amount"].Value = -50; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectContrast-50.jpg"); } }

Original Image

Contrast Amount 25

Contrast Amount 50

Contrast Amount -50

