# SaveAlpha Property

## Notes

This property determines whether the Save method includes an alpha channel in the rendered output.

Only some types of output support alpha. These are:

By including an alpha channel in your output you can identify areas which are transparent and areas on which no drawing has taken place.

## Example

The following example shows the effect that this parameter has on PDF rendering. We create a PDF with some text on it. We then render the PDF with an alpha channel and add the transparent image into a new PDF with a blue background. The blue background shows through where the image is transparent.

[C#] // Add some text Doc doc = new Doc(); doc.FontSize = 196; doc.TextStyle.HPos = 0.5; doc.TextStyle.VPos = 0.3; doc.AddText("Hello World"); // Render the PDF with alpha doc.Rendering.SaveAlpha = true; using var alphaBitmap = doc.Rendering.GetBitmap(); // Create a blue PDF doc = new Doc(); doc.Color.String = "0 0 255"; doc.FillRect(); // Add the transparent Bitmap into the PDF // so that the underlying blue can show through doc.AddImageBitmap(alphaBitmap, true); // Save render of pdf doc.Rendering.Save(Server.MapPath("RenderingSaveAlpha.png")); [Visual Basic] ' Add some text Dim doc As New Doc() doc.FontSize = 196 doc.TextStyle.HPos = 0.5 doc.TextStyle.VPos = 0.3 doc.AddText("Hello World") ' Render the PDF with alpha doc.Rendering.SaveAlpha = True Dim alphaBitmap As Bitmap = doc.Rendering.GetBitmap() ' Create a blue PDF doc = New Doc() doc.Color.String = "0 0 255" doc.FillRect() ' Add the transparent Bitmap into the PDF ' so that the underlying blue can show through doc.AddImageBitmap(alphaBitmap, True) ' Save render of pdf doc.Rendering.Save(Server.MapPath("RenderingSaveAlpha.png"))

RenderingSaveAlpha.png

Also see example code in: Page GetBitmap Function.

