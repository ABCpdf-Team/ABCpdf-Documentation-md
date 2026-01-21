---
title: "08-setparent"
css: "abcpdf-docs.css"
---

|  |  | SetParent Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets the parent of this structure element. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp SetParent(this StructureElementElement element, StructureElementElement parent) SetParent(this StructureElementElement element, StructureElementElement parent, int index) ``` [Visual Basic] ``` SetParent(this StructureElementElement element, StructureElementElement parent) SetParent(this StructureElementElement element, StructureElementElement parent, int index) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| parent | The parent which will adopt this structure element. | 
| index | The index at which the element should be inserted in the child array. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Sets the parent of this structure element. First this structure element is removed from any current parent. Then this structure element is inserted into the child array of the new parent. Optionally you can specify an index to determine the location in the child array. If no index is provided then the location will be at the end of the child array. |  |  | 
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