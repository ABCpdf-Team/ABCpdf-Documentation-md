---
title: "05-getpage"
css: "abcpdf-docs.css"
---

|  |  | GetPage Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the Page object for this particular structure element. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp GetPage(this StructureElementElement element) GetPage(this StructureElementElement element, Accessibility.Structure structure) ``` [Visual Basic] ``` GetPage(this StructureElementElement element) GetPage(this StructureElementElement element, Accessibility.Structure structure) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | The page. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Get the Page object for this particular structure element. In the event that there is no specified page the function will look up through the parent hierarchy to find one. If still no page is found it will scan through the hierarchy assigning pages to all the elements and then return one. In the unlikely event that no page can be found, it will return null. |  |  | 
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