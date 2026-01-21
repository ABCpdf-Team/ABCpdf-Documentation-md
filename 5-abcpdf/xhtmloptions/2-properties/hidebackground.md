# HideBackground Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to hide the background color of a page. | 

## Notes

Whether to to hide the background color of an HTML page.

This can be useful for making HTML pages with transparent backgrounds.

Note that the background color is not the same as a background image or tiled image. This property operates on background colors only.

## Example

The following example shows the effect that this parameter has on HTML rendering.

[C#]

```csharp
using var doc = new Doc();
// Please note that the URL below is included for demonstration purposes only.
// In your code you should use your own URL. The site at the URL below
// may include other opaque elements which may obscure our blue rectangle.
string url = "https://www.websupergoo.com/";
// Add some content
doc.Color.String = "0 255 255"; // light blue
doc.FillRect(200, 200);
// Hide the background of the HTML page so content shows through
doc.HtmlOptions.HideBackground = true;
doc.AddImageUrl(url);
// Save the document
doc.Save(Server.MapPath("HtmlOptionsHideBackground.pdf"));
```

**[Visual Basic]**

```vbnet
Using doc As New Doc()
  ' Please note that the URL below is included for demonstration purposes only.
  ' In your code you should use your own URL. The site at the URL below
  ' may include other opaque elements which may obscure our blue rectangle.
  Dim theURL As String = "https://www.websupergoo.com/"
  ' Add some content
  doc.Color.String = "0 255 255"
  ' light blue
  doc.FillRect(200, 200)
  ' Hide the background of the HTML page so content shows through
  doc.HtmlOptions.HideBackground = True
  doc.AddImageUrl(theURL)
  ' Save the document
  doc.Save(Server.MapPath("HtmlOptionsHideBackground.pdf"))
End Using
```

![](../../../images/pdf/HtmlOptionsHideBackground.pdf.png) HtmlOptionsHideBackground.pdf