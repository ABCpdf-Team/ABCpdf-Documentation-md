---
title: "2-forchrome"
css: "abcpdf-docs.css"
---

|  |  | ForChrome Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IHtmlChromeOptions ``` [Visual Basic] `IHtmlChromeOptions` | n/a | Yes | An object that provides access to only the HTML options supported by the ABCChrome engine. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The HTML options supported by the ABCChrome engine. ### Supported methods EndTasks GetHttpStatusCode GetScriptReturn GetTagIDs GetTagRects GetTagUntransformedRects LinkPages ### Supported properties AddForms AddLinks AddTags AddIDs AddNames BaseURI BrowserWidth FireShield HideBackground InitialWidth IgnoreCertificateErrors Media OnLoadScript ProcessOptions RepaintDelay RepaintTimeout RetryCount Timeout UseScript UseProxyServer |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD>&nbsp;</TD>
    <TD vAlign=top>
      
| [C#] ```csharp using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.Chrome123; doc.HtmlOptions.ForChrome.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForChrome; options.UseScript = false; options.AddTags = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg1.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.Chrome123 doc.HtmlOptions.ForChrome.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlChromeOptions = doc.HtmlOptions.ForChrome options.UseScript = False options.AddTags = True doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg1.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>