# SaveQuality Property

## Notes

This property determines the quality of the output image.

It can take values between 0 and 100 ranging from lowest to highest quality.

## Example

The following example shows the effect that this parameter has on PDF rendering.

[C#] using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/SpaceShuttlePage6.pdf")); doc.Rendering.DotsPerInch = 36; // Save at low quality doc.Rendering.SaveQuality = 5; doc.Rendering.Save(Server.MapPath("RenderingQuality5.jpg")); // Save at high quality doc.Rendering.SaveQuality = 75; doc.Rendering.Save(Server.MapPath("RenderingQuality75.jpg")); [Visual Basic] Using doc As New Doc() doc.Read(Server.MapPath("../mypics/SpaceShuttlePage6.pdf")) doc.Rendering.DotsPerInch = 36 ' Save at low quality doc.Rendering.SaveQuality = 5 doc.Rendering.Save(Server.MapPath("RenderingQuality5.jpg")) ' Save at high quality doc.Rendering.SaveQuality = 75 doc.Rendering.Save(Server.MapPath("RenderingQuality75.jpg")) End Using

RenderingQuality5.jpg [file size 9.26 KB]

RenderingQuality75.jpg [file size 37.3 KB]

