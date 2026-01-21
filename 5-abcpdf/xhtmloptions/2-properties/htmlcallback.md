---
title: "htmlcallback"
css: "abcpdf-docs.css"
---

|  |  | HtmlCallback Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp HtmlCallback ``` [Visual Basic]`HtmlCallback` | null | No | The multicast delegate to be called while HTML rendering is taking place. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This delegate is called during HTML rendering. During the time that HTML rendering is taking place delegates are called periodically. This gives a mechanism for tracking progress and for intercepting and modifying or querying pages on the fly. If the page is obtained from the cache then the delegate will not be called. Note that the amount of work done during a callback should be kept to a minimum. The definition of the HtmlCallback multicast delegate is as follows. [C#] ```csharp delegate void HtmlCallback(string stage, object page); ``` [Visual Basic] ```vbnet Delegate Sub HtmlCallback(stage As String, page As Object); ``` Current values for the stage variable are 'get width', 'get height' and 'render'. The first occurs prior to finding the natural width of the HTML (the width it can occupy without scrolling). The second occurs prior to finding the natural height. The third occurs prior to translation into PDF format. The page is provided via a mshtml.HTMLDocumentClass object - see Microsoft documentation for details. However note that while the interface is standard the behavior may not be identical. For example element positions may not be available. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following example shows the effect that this parameter has on HTML rendering. [C#] ```csharp using var doc = new Doc(); string uri = "https://photojournal.jpl.nasa.gov/catalog/PIA24312"; // Set up the callback var theLog = new StringBuilder(); doc.HtmlOptions.HtmlCallback = (string stage, object page) => theLog.AppendLine(stage); // Render html page doc.AddImageUrl(uri); // Add log over the top of the content doc.Rect.Inset(100, 100); doc.Color.String = "255 0 0"; doc.FontSize = 96; doc.AddText(theLog.ToString()); // Save the document doc.Save(Server.MapPath("HtmlOptionsCallback.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theURL As String = "https://photojournal.jpl.nasa.gov/catalog/PIA24312" ' Set up the callback Dim theLog As New StringBuilder() doc.HtmlOptions.HtmlCallback = Function(stage As String, page As Object) theLog.AppendLine(stage) ' Render html page doc.AddImageUrl(theURL) ' Add log over the top of the content doc.Rect.Inset(100, 100) doc.Color.String = "255 0 0" doc.FontSize = 96 doc.AddText(theLog.ToString()) ' Save the document doc.Save(Server.MapPath("HtmlOptionsCallback.pdf")) End Using ``` HtmlOptionsCallback.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>