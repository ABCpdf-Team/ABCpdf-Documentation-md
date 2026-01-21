---
title: "addlinks"
css: "abcpdf-docs.css"
---

# AddLinks Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether hyperlinks should be live. | 

## Notes

This property determines whether links in HTML are reproduced as links in the final PDF output.

Links which are not live look exactly like links but do not link through to a destination when you click on them.

Live links are reproduced exactly as specified on the page and link through to the web pages specified. These web pages will open in a new browser window.

To change external links to internal PDF links see the [Doc.LinkPages](../1-methods/linkpages.md) method.

## Example

See the [Doc.LinkPages](../1-methods/linkpages.md) method.

Also see example code in: [XHtmlOptions LinkDestinations Method](../1-methods/linkdestinations.md), [XHtmlOptions LinkPages Method](../1-methods/linkpages.md), [XHtmlOptions UseScript Property](usescript.md).