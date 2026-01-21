---
title: "flatten"
css: "abcpdf-docs.css"
---

|  |  | Flatten Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Flattens and compresses the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int Flatten() ``` [Visual Basic]`Function Flatten() As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | n/a. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Objects added to a page are stored as individual layers. Calling this method combines all the layers on the current page and then re-compresses the layer data. For pages that contain only a few layers the reduction in size will be minimal. However for pages which contain complex tables with many items, flattening can reduce the size of the output PDF by a factor of five or more. Note that flattening will delete all the items currently on the page and replace them with a new compressed item. This means that Object IDs previously obtained from calls such as AddText or FrameRect will no longer be valid. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Small Table Example and Large Table Example. Also see example code in: ABCpdf Small Table Example, ABCpdf Large Table Example, ABCpdf Paged HTML Example, Doc AddImageToChain Function, XHtmlOptions LinkDestinations Method, XHtmlOptions LinkPages Method, XHtmlOptions UseScript Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>