# ForGecko Property

## Notes

The HTML options supported by the ABCGecko HTML engine.

The HttpAdditionalHeaders property is supported under some circumstances but because these are unusual it is not included in this interface. For details see the documentation for this property.

## Example

[C#] using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.Gecko; doc.HtmlOptions.ForGecko.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForGecko; options.AddLinks = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save("wsg2.pdf");

