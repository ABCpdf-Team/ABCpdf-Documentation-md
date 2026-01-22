# Median Effect

## Settings

The width of the median filter to be applied.

## Workings

The median filter replaces each pixel with the median of its neighbors. The Median has a number of advantages over the Mean. Firstly unrepresentative pixels do not unduly influence the outcome of the final pixel level - this is why the filter is good at removing "salt and pepper" noise. Secondly, because the final pixel must actually be the value of one of its neighbors, edges are preserved more faithfully.

The image below show the neighboring pixels polled in a 4 by 3 Median Filter.

## Example

The following example images show the effect of a Median filter applied to a noisy picture at different width and height settings.

[C#] void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img5); // original image doc.Rendering.Save("EffectMedian.jpg"); using (ImageLayer layer = AddImagePage(doc, img5)) { using (EffectOperation effect = new EffectOperation("Median")) { effect.Parameters["Width"].Value = 3; effect.Parameters["Height"].Value = 3; effect.Parameters["X"].Value = 2; effect.Parameters["Y"].Value = 2; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectMedian3.jpg"); using (ImageLayer layer = AddImagePage(doc, img5)) { using (EffectOperation effect = new EffectOperation("Median")) { effect.Parameters["Width"].Value = 5; effect.Parameters["Height"].Value = 5; effect.Parameters["X"].Value = 3; effect.Parameters["Y"].Value = 3; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectMedian5.jpg"); using (ImageLayer layer = AddImagePage(doc, img5)) { using (EffectOperation effect = new EffectOperation("Median")) { effect.Parameters["Width"].Value = 9; effect.Parameters["Height"].Value = 9; effect.Parameters["X"].Value = 4; effect.Parameters["Y"].Value = 4; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectMedian9.jpg"); } } [Visual Basic] Sub ... Using doc As New Doc() AddImagePage(doc, img5) ' original image doc.Rendering.Save("EffectMedian.jpg") Using layer As ImageLayer = AddImagePage(doc, img5) Using effect As New EffectOperation("Median") effect.Parameters("Width").Value = 3 effect.Parameters("Height").Value = 3 effect.Parameters("X").Value = 2 effect.Parameters("Y").Value = 2 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectMedian3.jpg") Using layer As ImageLayer = AddImagePage(doc, img5) Using effect As New EffectOperation("Median") effect.Parameters("Width").Value = 5 effect.Parameters("Height").Value = 5 effect.Parameters("X").Value = 3 effect.Parameters("Y").Value = 3 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectMedian5.jpg") Using layer As ImageLayer = AddImagePage(doc, img5) Using effect As New EffectOperation("Median") effect.Parameters("Width").Value = 9 effect.Parameters("Height").Value = 9 effect.Parameters("X").Value = 4 effect.Parameters("Y").Value = 4 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectMedian9.jpg") End Using End Sub

Original Image before Median Filter

Width = 3, Height = 3, X = 2, Y = 2

Width = 5, Height = 5, X = 3, Y = 3

Width = 9, Height = 9, X = 4, Y = 4

