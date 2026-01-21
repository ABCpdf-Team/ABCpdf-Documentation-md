---
title: "2-forwebkit"
css: "abcpdf-docs.css"
---

|  |  | ForWebKit Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IHtmlWebKitOptions ``` [Visual Basic] `IHtmlWebKitOptions` | n/a | Yes | An object that provides access to only the HTML options supported by the ABCWebKit engine. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The HTML options supported by the ABCWebKit engine. ### Supported methods EndTasks ### Supported properties AddLinks BrowserWidth FireShield HideBackground Media OnLoadScript ProcessOptions RepaintTimeout [but not RepaintDelay] RetryCount Timeout UseScript |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD>&nbsp;</TD>
    <TD vAlign=top>
      
| [C#] ```csharp using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.WebKit; doc.HtmlOptions.ForWebKit.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForWebKit; options.UseScript = false; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg4.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.WebKit doc.HtmlOptions.ForWebKit.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlWebKitOptions = doc.HtmlOptions.ForWebKit options.UseScript = False doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg4.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>