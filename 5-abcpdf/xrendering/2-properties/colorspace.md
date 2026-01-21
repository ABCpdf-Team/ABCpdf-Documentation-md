---
title: "colorspace"
css: "abcpdf-docs.css"
---

# ColorSpace Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp XRendering.ColorSpaceType ``` [Visual Basic] `XRendering.ColorSpaceType` | XRendering.ColorSpaceType.Rgb | No | The name of the output color space. | 

## Notes

The name of the output color space.

The XRendering.ColorSpaceType enumeration may take the following values:

- Rgb - red, green and blue
- Gray - grayscale
- Cmyk - cyan, magenta, yellow and black
- Lab - a device independent color space
- Indexed - indexed RGB; see the [Palette](palette.md) property

The following table shows the supported color spaces and valid [BitsPerChannel](bitsperchannel.md) for each output format:

| Output format | RGB | Gray | CMYK | Lab | Indexed | 
| --- | --- | --- | --- | --- | --- |
| TIFF | 8, 16 | 1, 8, 16 | 8, 16 | 8, 16 |  | 
| PSD (Photoshop) | 8, 16 | 8, 16 | 8, 16 | 8, 16 |  | 
| JP2 (JPEG 2000) | 8, 16 | 8, 16 | 8, 16 |  |  | 
| JPG | 8 | 8 | 8 |  |  | 
| BMP | 8 | 8 |  |  | 8 | 
| PNG | 8 | 8, 16 |  |  | 8 | 
| GIF | 8 (8 bit indexed) | 8 |  |  | 8 | 

Why is my ColorSpace a string?

In older versions of ABCpdf the ColorSpace property was a string. So you might find code of this form.

[C#]

```csharp
theDoc.Rendering.ColorSpace = "CMYK";
```

**[Visual Basic]**

```vbnet
theDoc.Rendering.ColorSpace = "CMYK"
```

In Version 8 the ColorSpace property was changed to a true enumeration. This is a safer way of coding as it allows the compiler to ensure that the values you are using are valid. Your new code should look like this.

[C#]

```csharp
theDoc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk;
```

**[Visual Basic]**

```vbnet
theDoc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk
```

The names of the items in the XRendering.ColorSpaceType enumeration are the same as the values of the strings used in previous versions. So changing your code should be a simple search and replace operation.

Note that the enumeration is the XRendering.ColorSpace indicating the output color space for rendering. There is a different ColorSpace enumeration used for the content of objects inside a PDF document. The two are not the same.

Alternatively if you need to convert between enumerations and strings automatically you can do so. To convert from a string to an enumeration use the following code.

[C#]

```csharp
XRendering.ColorSpaceType csType = (XRendering.ColorSpaceType)Enum.Parse(typeof(XRendering.ColorSpaceType), csString, true);
```

**[Visual Basic]**

```vbnet
Dim csType As XRendering.ColorSpaceType = CType([Enum].Parse(GetType(XRendering.ColorSpaceType), csString, True), XRendering.ColorSpaceType)
```

To convert from an enumeration to a string use the following code.

[C#]

```csharp
string csString = csType.ToString("G");
```

**[Visual Basic]**

```vbnet
Dim csString As String = csType.ToString("G")
```

## Example

The following example shows the effect that this parameter has on PDF rendering.

[C#]

```csharp
using var doc = new Doc();
doc.AddImage(Server.MapPath("../mypics/Shuttle.jpg"));
doc.Rect.String = doc.MediaBox.String;
// Render document in Gray colorspace
doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray;
doc.Rendering.DotsPerInch = 36;
doc.Rendering.Save(Server.MapPath("RenderingColorSpace.png"));
```

**[Visual Basic]**

```vbnet
Using doc As New Doc()
  doc.AddImage(Server.MapPath("../mypics/Shuttle.jpg"))
  doc.Rect.String = doc.MediaBox.[String]
  ' Render document in Gray colorspace
  doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray
  doc.Rendering.DotsPerInch = 36
  doc.Rendering.Save(Server.MapPath("RenderingColorSpace.png"))
End Using
```

![](../../../images/pdf/Shuttle.jpg) Shuttle.jpg

![](../../../images/pdf/RenderingColorSpace.png) RenderingColorSpace.png

Also see example code in: [XRendering DefaultHalftone Property](defaulthalftone.md), [XRendering IccCmyk Property](icccmyk.md), [XRendering Overprint Property](overprint.md), [XRendering SaveCompression Property](savecompression.md).