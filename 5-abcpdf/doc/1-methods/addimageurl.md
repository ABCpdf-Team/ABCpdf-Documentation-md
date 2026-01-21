---
title: "addimageurl"
css: "abcpdf-docs.css"
---

|  |  | AddImageUrl Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Renders a web page specified by URL. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddImageUrl(string url) int AddImageUrl(string url, bool paged, int width, bool disableCache) ``` [Visual Basic] ``` Function AddImageUrl(url As String) As Integer Function AddImageUrl(url As String, paged As Boolean, width As Integer, disableCache As Boolean) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| url | The URL for the page to be rendered. The actual value may be modified depending on the value of disableCache/XHtmlOptions.PageCacheEnabled. | 
| paged | Allows you to override the default XHtmlOptions.Paged property. | 
| width | Allows you to override the default XHtmlOptions.BrowserWidth property. | 
| disableCache | Allows you to override and disable the page cache. See the XHtmlOptions.PageCacheEnabled property for details. | 
| return | The ID of the newly added object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method adds a web page to a document. The page is added in accordance with the current XHtmlOptions settings. As a convenience you can override the more commonly used settings as detailed above. Only the first page of the document is drawn. Subsequent pages can be drawn using the AddImageToChain method. The web page is scaled to fill the current Rect. It is transformed using the current Transform. Caching. Sometimes you may find that pages appear to be cached. If you are using AddImageUrl it is possible that the URL is in some way being cached. So the PDF may be changing but the content within it may be staying the same. See the HTML / CSS Rendering section of the documentation for details. Alternatively it is possible that the PDF itself is being cached. Most commonly this can happen if you're streaming the PDF direct to the browser and you have certain IIS settings (like Expire Content) disabled. Your first step should be to narrow down the problem. Why not save the PDF to disk at the same time as sending it to the client? That way you can establish whether the PDF itself is being cached or whether the content is in some way being cached (resulting in the same PDF being created again and again). If the PDF is being cached you will need to look at your IIS settings. ABCpdf is not doing the caching (and indeed it cannot cache the PDF in this way) it will be something which is happening either in IIS/ASP or on an intervening proxy server or on the client. | 
| --- |

In addition to accepting URLs to web pages, this method also accepts file based URLs to MHT (MIME HTML) files.

MHT files contain a web page and any associated resources (such as images and style sheets) in one compact archive. You can save web pages in MHT format using IE.

Note that MHT files saved from more complex web pages sometimes omit some required resources. In this situation ABCpdf will attempt to download missing items from the original URL on the web. However if these items are no longer available then ABCpdf may not be able to produce a perfect output.

Make sure your URLs come from trusted sources. See the Security section of the [HTML / CSS Rendering](../../../3-concepts/g-htmlrender.md) section of the documentation for details.

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| We create an ABCpdf Doc object, add our URL and save. That's it! [C#] ```csharp using var doc = new Doc(); doc.AddImageUrl("http://www.google.com/"); doc.Save(Server.MapPath("htmlimport.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.AddImageUrl("http://www.google.com/") doc.Save(Server.MapPath("htmlimport.pdf")) End Using ``` htmlimport.pdf For an example of how to use paged HTML see the AddImageToChain method. Also see example code in: XHtmlOptions ForChrome Property, XHtmlOptions ForGecko Property, XHtmlOptions ForMSHtml Property, XHtmlOptions ForWebKit Property, XHtmlOptions BrowserWidth Property, XHtmlOptions HideBackground Property, XHtmlOptions HtmlCallback Property, XHtmlOptions HtmlEmbedCallback Property, XHtmlOptions ImageQuality Property, XHtmlOptions LogonName Property, XHtmlOptions RetryCount Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>