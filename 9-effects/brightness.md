# Brightness Effect

## Settings

Amount to lighten or darken the image.

## Workings

The value given is added to every pixel in the image. The value may be negative in which case the result is to darken rather than lighten the image.

## Example

The following show the effect of brightening or darkening an image.

[C#] void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img2); // original image doc.Rendering.Save("EffectBrightness.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Brightness")) { effect.Parameters["Amount"].Value = 20; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectBrightness20.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Brightness")) { effect.Parameters["Amount"].Value = -20; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectBrightness-20.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Brightness")) { effect.Parameters["Amount"].Value = 60; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectBrightness60.jpg"); } }

Original Image

Brightness Amount 20

Brightness Amount -20

Brightness Amount 60

