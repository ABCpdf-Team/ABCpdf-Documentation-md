---
title: "addimageurl"
css: "abcpdf-docs.css"
---

# AddImageUrl Function

Renders a web page specified by URL.

## Syntax

**[C#]**

```csharp
int AddImageUrl(string url)
int AddImageUrl(string url, bool paged, int width, bool disableCache)
```

<span class=language>[Visual Basic]</span>  

```
Function AddImageUrl(url As String) As Integer
Function AddImageUrl(url As String, paged As Boolean, width As Integer, disableCache As Boolean) As Integer
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| url | The URL for the page to be rendered. The actual value may be modified depending on the value of disableCache/XHtmlOptions.PageCacheEnabled. | 
| paged | Allows you to override the default XHtmlOptions.Paged property. | 
| width | Allows you to override the default XHtmlOptions.BrowserWidth property. | 
| disableCache | Allows you to override and disable the page cache. See the XHtmlOptions.PageCacheEnabled property for details. | 
| return | The ID of the newly added object. | 

## Notes

This method adds a web page to a document.

The page is added in accordance with the current [XHtmlOptions](../../xhtmloptions/default.md) settings. As a convenience you can override the more commonly used settings as detailed above.

Only the first page of the document is drawn. Subsequent pages can be drawn using the [AddImageToChain](addimagetochain.md) method.

The web page is scaled to fill the current [Rect](../2-properties/rect.md). It is transformed using the current [Transform](../../xtransform/default.md).

Caching. Sometimes you may find that pages appear to be cached.

If you are using AddImageUrl it is possible that the URL is in some way being cached. So the PDF may be changing but the content within it may be staying the same. See the [HTML / CSS Rendering](../../../3-concepts/g-htmlrender.md) section of the documentation for details.

Alternatively it is possible that the PDF itself is being cached. Most commonly this can happen if you're streaming the PDF direct to the browser and you have certain IIS settings (like Expire Content) disabled.

Your first step should be to narrow down the problem. Why not save the PDF to disk at the same time as sending it to the client? That way you can establish whether the PDF itself is being cached or whether the content is in some way being cached (resulting in the same PDF being created again and again).

If the PDF is being cached you will need to look at your IIS settings. ABCpdf is not doing the caching (and indeed it cannot cache the PDF in this way) it will be something which is happening either in IIS/ASP or on an intervening proxy server or on the client.

In addition to accepting URLs to web pages, this method also accepts file based URLs to MHT (MIME HTML) files.

MHT files contain a web page and any associated resources (such as images and style sheets) in one compact archive. You can save web pages in MHT format using IE.

Note that MHT files saved from more complex web pages sometimes omit some required resources. In this situation ABCpdf will attempt to download missing items from the original URL on the web. However if these items are no longer available then ABCpdf may not be able to produce a perfect output.

Make sure your URLs come from trusted sources. See the Security section of the [HTML / CSS Rendering](../../../3-concepts/g-htmlrender.md) section of the documentation for details.

## Example

We create an ABCpdf Doc object, add our URL and save. That's it!

[C#]

```csharp
using var doc = new Doc();
doc.AddImageUrl("http://www.google.com/");
doc.Save(Server.MapPath("htmlimport.pdf"));
```

<span class=language>[Visual
            Basic]</span>
```vbnet
Using doc As New Doc()
  doc.AddImageUrl("http://www.google.com/")
  doc.Save(Server.MapPath("htmlimport.pdf"))
End Using
```

![](../../../images/pdf/htmlimport.pdf.png)htmlimport.pdf

For an example of how to use paged HTML see the [AddImageToChain](addimagetochain.md) method.

Also see example code in: [XHtmlOptions ForChrome Property](../../xhtmloptions/2-properties/2-forchrome.md), [XHtmlOptions ForGecko Property](../../xhtmloptions/2-properties/2-forgecko.md), [XHtmlOptions ForMSHtml Property](../../xhtmloptions/2-properties/2-formshtml.md), [XHtmlOptions ForWebKit Property](../../xhtmloptions/2-properties/2-forwebkit.md), [XHtmlOptions BrowserWidth Property](../../xhtmloptions/2-properties/browserwidth.md), [XHtmlOptions HideBackground Property](../../xhtmloptions/2-properties/hidebackground.md), [XHtmlOptions HtmlCallback Property](../../xhtmloptions/2-properties/htmlcallback.md), [XHtmlOptions HtmlEmbedCallback Property](../../xhtmloptions/2-properties/htmlembedcallback.md), [XHtmlOptions ImageQuality Property](../../xhtmloptions/2-properties/imagequality.md), [XHtmlOptions LogonName Property](../../xhtmloptions/2-properties/logonname.md), [XHtmlOptions RetryCount Property](../../xhtmloptions/2-properties/retrycount.md).