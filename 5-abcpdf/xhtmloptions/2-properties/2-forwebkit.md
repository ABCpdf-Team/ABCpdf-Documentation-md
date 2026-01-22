# ForWebKit Property

## Notes

The HTML options supported by the ABCWebKit engine.

## Example

[C#] using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.WebKit; doc.HtmlOptions.ForWebKit.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForWebKit; options.UseScript = false; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg4.pdf")); [Visual Basic] Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.WebKit doc.HtmlOptions.ForWebKit.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlWebKitOptions = doc.HtmlOptions.ForWebKit options.UseScript = False doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg4.pdf")) End Using

