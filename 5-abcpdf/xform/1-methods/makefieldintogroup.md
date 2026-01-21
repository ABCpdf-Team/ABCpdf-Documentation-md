---
title: "makefieldintogroup"
css: "abcpdf-docs.css"
---

|  |  | MakeFieldIntoGroup Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Make duplicate fields into synchronized groups. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool MakeFieldIntoGroup(Field inField) ``` [Visual Basic] ``` Function MakeFieldIntoGroup(inField As Field) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| inField | The field to operate on | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Make duplicate fields into synchronized groups. Scans through sibling fields looking for duplicate names. Any duplicates are put together in a field group so that they will synchronize. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Annotations example project. None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>