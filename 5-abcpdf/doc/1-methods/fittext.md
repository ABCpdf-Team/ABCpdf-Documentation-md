---
title: "fittext"
css: "abcpdf-docs.css"
---

|  |  | FitText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Fit a block of text into the current rectangle on the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int FitText(string text) ``` [Visual Basic] ``` Function FitText(text As String) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | The text to be added to the page. | 
| return | The Object ID of the newly added Text Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Fit a block of text into the current rectangle on the current page. This function is similar to AddText but can be used in situations in which you have a set area into which you know your text should be fitted. The call will take the base text supplied and scale it appropriately until it fits as exactly as possible into the current Rect. For fitting multi-styled text you should use the FitTextStyled method which is used for adding styled text. |  |  | 
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