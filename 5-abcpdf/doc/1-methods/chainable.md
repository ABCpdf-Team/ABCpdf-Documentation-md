---
title: "chainable"
css: "abcpdf-docs.css"
---

|  |  | Chainable Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Determines if an object is chainable. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Chainable(int id) ``` [Visual Basic]`Function Chainable(id As Integer) As Boolean` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the object to be tested. | 
| return | Whether the object is chainable or not. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to determine if an object is chainable. Some objects can be chained. A chunk of text may be chained from page to page on the output PDF. Similarly a web page may be chained from page to page. This method allows you to determine if the object you have added is chainable or whether it is at the end of the chain. Only text, PostScript images and web pages can be chainable. So your ID should have been obtained from a previous call to one of the AddImage family of calls or from AddTextStyled. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the AddImageToChain method. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>