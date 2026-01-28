# ForMSHtml Property

## Notes

The HTML options supported by the MSHTML engine.

## Example

[C#] using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.MSHtml; doc.HtmlOptions.ForMSHtml.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForMSHtml; options.UseActiveX = true; options.AutoTruncate = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save("wsg3.pdf");

