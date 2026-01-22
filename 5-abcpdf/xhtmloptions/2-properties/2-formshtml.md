# ForMSHtml Property

## Notes

The HTML options supported by the MSHTML engine.

## Example

[C#] using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.MSHtml; doc.HtmlOptions.ForMSHtml.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForMSHtml; options.UseActiveX = true; options.AutoTruncate = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg3.pdf")); [Visual Basic] Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.MSHtml doc.HtmlOptions.ForMSHtml.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlMSHtmlOptions = doc.HtmlOptions.ForMSHtml options.UseActiveX = True options.AutoTruncate = True doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg3.pdf")) End Using

