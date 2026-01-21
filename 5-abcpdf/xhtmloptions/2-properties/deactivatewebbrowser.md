---
title: "deactivatewebbrowser"
css: "abcpdf-docs.css"
---

|  |  | DeactivateWebBrowser Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic]`Boolean` | true | No | Whether to deactivate the WebBrowser. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property determines whether the WebBrowser is deactivated before rendering. By default, if vector-output coercion is not activated, the WebBrowser is deactivated because an active WebBrowser may produce a rasterized output. In some cases, you may want to set this to false and possibly disable vector-output coercion in order to render pages, such as Google Maps, that require the WebBrowser to be active. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>