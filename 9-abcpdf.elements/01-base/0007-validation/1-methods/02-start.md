---
title: "02-start"
css: "abcpdf-docs.css"
---

|  |  | Start Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called at the point each Element starts validation. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual bool Start(Element element) virtual void Start(string entry) virtual void Start(int index) ``` [Visual Basic] ``` Overridable Function Start(element As Element) As Boolean Overridable Function Start(entry As string) As void Overridable Function Start(index As int) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| element | The element. | 
| entry | The new key or entry. | 
| index | The new index. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called at the point each Element starts validation. If the Element has already been seen then this function should return false to indicate that it has already been validated. If not then the function should return true to indicate that validation should go ahead. Subclasses should keep track of elements that they have seen so as to avoid recursive loops. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>