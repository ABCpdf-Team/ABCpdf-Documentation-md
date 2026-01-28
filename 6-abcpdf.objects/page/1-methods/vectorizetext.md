# VectorizeText Function

## Syntax

[C#]void VectorizeText()

may throw Exception()

## Params

## Notes

Use this method to vectorize the text (i.e. replace the text with equivalent glyph polygon outlines).

Note that pages may sometimes share content with other pages. If this is the case then vectorizing the text on one page will also vectorize it on other pages which use this shared content.

## Example

[C#] using var doc = new Doc(); doc.FontSize = 96; doc.AddText("Hello World"); foreach (var page in doc.ObjectSoup.Catalog.Pages.GetPageArrayAll()) page.VectorizeText(); doc.Save("VectorizedText.pdf");

