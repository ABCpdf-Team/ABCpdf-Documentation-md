# Levels Effect

The Levels effect allows you fine control over brightness and contrast.

## Settings

| Name | Default | Description | 
| --- | --- | --- |
| Black Input | 0 % | The level in the current image that should be regarded as black. | 
| White Input | 100 % | The level in the current image that should be regarded as white. | 
| Black Output | 0 % | The level in the final image that should be regarded as black. | 
| White Output | 100 % | The level in the final image that should be regarded as white. | 

## Workings

Well defined images span an entire range of color intensities. However it is common to find images that do not. If a photo has been overexposed it will be too bright - there will be few colors at the low ends of intensity and many at the high end. Similarly if a photograph has been underexposed it will be very dark - all the colors will be at the low end of the range and virtually none at the high end.

The Levels effect allows you fine control over brightness and contrast to let you correct this kind of problem. The basic method of adjustment is to set the black and white points on the input image. Normally the black point will be at 0 and the white point at 255. This simply means that black is represented by the value 0 and white is represented by the value 255.

However if an image is too dark there may be no pixels at all with a value of 255. In this case what was white on the original image might be represented by a value of only 200. By setting the white input point to 200 and then applying the effect, the levels in between will be stretched to try and restore balance to the image. A similar operation setting the black input point would apply if an image was too light.

As well as being able to specify input points you can also specify output points. This lets you tell the effect what value should be regarded as white and black on the final output image.

The levels effect is often used in conjunction with an image histogram so that the exact representation of different color levels can be seen in the image.

## Example

The following example images show the effect of the Levels effect.

[C#]

```csharp
void function() {
  using (Doc doc = new Doc()) {
    AddImagePage(doc, img6); // original image
    doc.Rendering.Save("EffectLevels.jpg");
    using (ImageLayer layer = AddImagePage(doc, img6)) {
      using (EffectOperation effect = new EffectOperation("Levels")) {
        effect.Parameters["White Input"].Value = 80;
        effect.Apply(layer.PixMap);
      }
    }
    doc.Rendering.Save("EffectLevelsWI80.jpg");
    using (ImageLayer layer = AddImagePage(doc, img6)) {
      using (EffectOperation effect = new EffectOperation("Levels")) {
        effect.Parameters["Black Input"].Value = 20;
        effect.Apply(layer.PixMap);
      }
    }
    doc.Rendering.Save("EffectLevelsBI20.jpg");
    using (ImageLayer layer = AddImagePage(doc, img6)) {
      using (EffectOperation effect = new EffectOperation("Levels")) {
        effect.Parameters["White Output"].Value = 80;
        effect.Apply(layer.PixMap);
      }
    }
    doc.Rendering.Save("EffectLevelsWO80.jpg");
  }
}
```

<span class=language>[Visual Basic]</span>
```vbnet
Sub ...
  Using doc As New Doc()
    AddImagePage(doc, img6)
    ' original image
    doc.Rendering.Save("EffectLevels.jpg")
    Using layer As ImageLayer = AddImagePage(doc, img6)
      Using effect As New EffectOperation("Levels")
        effect.Parameters("White Input").Value = 80
        effect.Apply(layer.PixMap)
      End Using
    End Using
    doc.Rendering.Save("EffectLevelsWI80.jpg")
    Using layer As ImageLayer = AddImagePage(doc, img6)
      Using effect As New EffectOperation("Levels")
        effect.Parameters("Black Input").Value = 20
        effect.Apply(layer.PixMap)
      End Using
    End Using
    doc.Rendering.Save("EffectLevelsBI20.jpg")
    Using layer As ImageLayer = AddImagePage(doc, img6)
      Using effect As New EffectOperation("Levels")
        effect.Parameters("White Output").Value = 80
        effect.Apply(layer.PixMap)
      End Using
    End Using
    doc.Rendering.Save("EffectLevelsWO80.jpg")
  End Using
End Sub
```

![](images/bouy2.jpg) Original Image

![](images/levels/wi200.jpg) White Input = 80

![](images/levels/bi50.jpg) Black Input = 20

![](images/levels/wo200.jpg) White Output = 80