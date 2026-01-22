# ColorSpace Property

## Notes

The name of the output color space.

The XRendering.ColorSpaceType enumeration may take the following values:

The following table shows the supported color spaces and valid BitsPerChannel for each output format:

Why is my ColorSpace a string?

In older versions of ABCpdf the ColorSpace property was a string. So you might find code of this form.

[C#] theDoc.Rendering.ColorSpace = "CMYK"; [Visual Basic] theDoc.Rendering.ColorSpace = "CMYK"

In Version 8 the ColorSpace property was changed to a true enumeration. This is a safer way of coding as it allows the compiler to ensure that the values you are using are valid. Your new code should look like this.

[C#] theDoc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk; [Visual Basic] theDoc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk

The names of the items in the XRendering.ColorSpaceType enumeration are the same as the values of the strings used in previous versions. So changing your code should be a simple search and replace operation.

Note that the enumeration is the XRendering.ColorSpace indicating the output color space for rendering. There is a different ColorSpace enumeration used for the content of objects inside a PDF document. The two are not the same.

Alternatively if you need to convert between enumerations and strings automatically you can do so. To convert from a string to an enumeration use the following code.

[C#] XRendering.ColorSpaceType csType = (XRendering.ColorSpaceType)Enum.Parse(typeof(XRendering.ColorSpaceType), csString, true); [Visual Basic] Dim csType As XRendering.ColorSpaceType = CType([Enum].Parse(GetType(XRendering.ColorSpaceType), csString, True), XRendering.ColorSpaceType)

To convert from an enumeration to a string use the following code.

[C#] string csString = csType.ToString("G"); [Visual Basic] Dim csString As String = csType.ToString("G")

## Example

The following example shows the effect that this parameter has on PDF rendering.

[C#] using var doc = new Doc(); doc.AddImage(Server.MapPath("../mypics/Shuttle.jpg")); doc.Rect.String = doc.MediaBox.String; // Render document in Gray colorspace doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray; doc.Rendering.DotsPerInch = 36; doc.Rendering.Save(Server.MapPath("RenderingColorSpace.png")); [Visual Basic] Using doc As New Doc() doc.AddImage(Server.MapPath("../mypics/Shuttle.jpg")) doc.Rect.String = doc.MediaBox.[String] ' Render document in Gray colorspace doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray doc.Rendering.DotsPerInch = 36 doc.Rendering.Save(Server.MapPath("RenderingColorSpace.png")) End Using

Shuttle.jpg

RenderingColorSpace.png

Also see example code in: XRendering DefaultHalftone Property, XRendering IccCmyk Property, XRendering Overprint Property, XRendering SaveCompression Property.

