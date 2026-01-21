---
title: "05-updateactualtext"
css: "abcpdf-docs.css"
---

|  |  | UpdateActualText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The logical structure can contain a copy of text which is drawn on the page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void UpdateActualText(bool erase, bool regenerate) ``` [Visual Basic] ``` Function UpdateActualText(erase As bool, regenerate As bool) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| erase | Whether existing actual text should be removed. | 
| regenerate | Whether actual text should be regenerated where possible. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The logical structure can contain a copy of text which is drawn on the page. This is held in the logical structure because it is to get hold or and also because it may be subtly different. For example the text "ll" might be represented using a single ligature in the page content,. whereas the text in the logical structure might use a double 'l'. One is optimized for display. The other is optimized for semantic accuracy. In cases where text on the page is changed the actual text may no longer be correct. In particular, if text is redacted, you do not want a copy of the text to be maintained. This function updates the actual text in the structure. |  |  | 
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