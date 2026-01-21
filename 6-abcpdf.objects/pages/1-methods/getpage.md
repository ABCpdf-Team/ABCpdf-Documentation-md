---
title: "getpage"
css: "abcpdf-docs.css"
---

|  |  | GetPage Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Performs a fast lookup to retrieve a particular Page from this node tree |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Page GetPage(int page) ``` [Visual Basic] ``` Function GetPage(Integer page) As Page ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| page | The page number - a one based index | 
| returns | The specified Page object or null if one could not be found. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Performs a fast lookup to retrieve a particular Page from this node tree. The page is specified in terms of the index of the page within the tree. This is a one-based index within the current Pages node. Since a Pages node relates to only a portion of a PDF document, the page number within the Pages node is offset from the page number within the document. |  |  | 
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