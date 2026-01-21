---
title: "vectorizetext"
css: "abcpdf-docs.css"
---

# VectorizeText Function

Replaces the text on the page with glyph outlines.

## Syntax

**[C#]**

```csharp
void VectorizeText()
```

**[Visual Basic]**
  
`Sub VectorizeText()`
										`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| none |  | 

## Notes

Use this method to vectorize the text (i.e. replace the text with equivalent glyph polygon outlines).

Note that pages may sometimes share content with other pages. If this is the case then vectorizing the text on one page will also vectorize it on other pages which use this shared content.

## Example

[C#]

```csharp
using var doc = new Doc();
doc.FontSize = 96;
doc.AddText("Hello World");
foreach (var page in doc.ObjectSoup.Catalog.Pages.GetPageArrayAll())
  page.VectorizeText();
doc.Save(Server.MapPath("VectorizedText.pdf"));
```

**[Visual Basic]**

```vbnet
Using doc As New Doc()
  doc.FontSize = 96
  doc.AddText("Hello World")
  For Each page As Page In doc.ObjectSoup.Catalog.Pages.GetPageArrayAll()
    page.VectorizeText()
  Next
  doc.Save(Server.MapPath("VectorizedText.pdf"))
End Using
```