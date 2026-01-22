# LinkDestinations Method

Convert a restricted selection of external links to internal links.

## Syntax

[C#]

```csharp
int LinkDestinations(IEnumerable&lt;int&gt; ids)int LinkDestinations(IEnumerable&lt;int&gt; linkIDs, IEnumerable&lt;int&gt; destIDs, bool linkPages)
```

[Visual Basic]

```vb
Sub LinkDestinations(ids As IEnumerable(Of Integer))Sub LinkDestinations(linkIDs As IEnumerable(Of Integer), destIDs As IEnumerable(Of Integer), linkPages As Boolean)
```

## Params

| **Name** | **Description** |
| --- | --- |
| ids | Specifies both linkIDs and destIDs. |
| linkIDs | The list of IDs of view objects containing links (anchor tags with href attributes). |
| destIDs | The list of IDs of view objects containing destinations (anchor tags with name attributes). |
| linkPages | Whether links pointing to the URLs of HTML pages (URLs without fragments) are converted to internal links. The default value is false. |
| return | The number of links converted. |

## Notes

This method scans the view objects specified in linkIDs converting external links to internal links where the destinations are found in the view objects specified in destIDs. It is similar to the [LinkPages](linkpages.md) method but allows you to restrict the conversion to lists of view objects.

By default, links in rendered HTML are preserved as is. This means that links in a web page link to external URLs. When you click on them, a browser window will be launched and the original target of the link displayed.

In some situations, you may wish to resolve links within the document so that they take you between pages in the PDF rather than launching an external browser window.

For example, you might add a number of web pages which contain links to each other. Rather than linking to the pages on the original web site, you might like to resolve the links so that they point at the pages as they now appear in the PDF.

Similarly, if you use named destinations (HTML fragments) with links within the document, you will may wish to use this method to convert them from external links to internal ones.

## Example

This example shows how to import an HTML page which uses named destinations. We first create a [Doc](default.md) object and inset the edges a little so that the HTML will appear in the middle of the page. We assign the appropriate HTML options so that links will be rendered live.

[C#]

```csharp
using var doc = new Doc();
doc.Rect.Inset(18, 18);
doc.HtmlOptions.AddLinks = true;
```

[Visual Basic]

```vb
Using doc As New Doc()
  doc.Rect.Inset(18, 18)
  doc.HtmlOptions.AddLinks = True
```

![](../../../images/pdf/linkpages.pdf.png)
linkpages.pdf [Page 1]

