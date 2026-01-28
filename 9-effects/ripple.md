# Ripple Effect

## Settings

The amplitude of the wave determines how high the ripples are on the surface of the images.

The length of the wave determines how far apart the ripples are placed.

## Workings

The effect is very similar to a pond ripple. The image is distorted as if it was projected onto the surface of a pond and then a stone had been dropped into the middle.

## Example

The following example images show the effect of a Ripple filter applied to a picture with different settings.

[C#] void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img3); // original image doc.Rendering.Save("EffectRipple.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Ripple")) { effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectRippleDefault.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Ripple")) { effect.Parameters["Height"].Value = 15; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectRippleHeight15.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Ripple")) { effect.Parameters["Length"].Value = 10; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectRippleLength10.jpg"); } }

Original Image before Ripple

After Ripple with default settings

Height = 15

Length = 10

