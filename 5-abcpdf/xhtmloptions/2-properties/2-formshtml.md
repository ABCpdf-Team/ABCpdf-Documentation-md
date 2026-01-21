---
title: "2-formshtml"
css: "abcpdf-docs.css"
---

|  |  | ForMSHtml Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IHtmlMSHtmlOptions ``` [Visual Basic] `IHtmlMSHtmlOptions` | n/a | Yes | An object that provides access to only the HTML options supported by the MSHTML engine. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The HTML options supported by the MSHTML engine. ### Supported methods GetHttpStatusCode GetScriptReturn GetTagIDs GetTagRects GetTagUntransformedRects LinkDestinations LinkPages PageCacheClear PageCachePurge SetTheme ### Supported properties AddForms AddLinks AddMovies AddTags AdjustLayout AutoTruncate BreakMethod BreakZoneSize BrowserWidth CoerceVector ContentCount DeactivateWebBrowser DisableVectorCoercion DoMarkup FontEmbed FontProtection FontSubset FontSubstitute HideBackground HostWebBrowser HtmlCallback HtmlEmbedCallback HttpAdditionalHeaders ImageQuality InitialWidth LogonName LogonPassword MakeFieldNamesUnique MaxAtomicImageSize NoCookie NoTheme OnLoadScript PageCacheEnabled PageCacheExpiry PageCacheSize Paged PageLoadMethod ProcessOptions (See MSHtmlBootstrap) ReloadPage RequestMethod RetryCount TargetLinks Timeout TransferModule UseActiveX UseJava UseNoCache UserAgent UseResync UseScript UseTheme UseVideo |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD>&nbsp;</TD>
    <TD vAlign=top>
      
| [C#] ```csharp using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.MSHtml; doc.HtmlOptions.ForMSHtml.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForMSHtml; options.UseActiveX = true; options.AutoTruncate = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg3.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.MSHtml doc.HtmlOptions.ForMSHtml.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlMSHtmlOptions = doc.HtmlOptions.ForMSHtml options.UseActiveX = True options.AutoTruncate = True doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg3.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>