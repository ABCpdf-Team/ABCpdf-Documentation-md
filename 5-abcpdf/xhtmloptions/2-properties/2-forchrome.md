# ForChrome Property

## Notes

The HTML options supported by the ABCChrome engine.

## Example

[C#] using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.Chrome123; doc.HtmlOptions.ForChrome.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForChrome; options.UseScript = false; options.AddTags = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg1.pdf")); [Visual Basic] Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.Chrome123 doc.HtmlOptions.ForChrome.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlChromeOptions = doc.HtmlOptions.ForChrome options.UseScript = False options.AddTags = True doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg1.pdf")) End Using

