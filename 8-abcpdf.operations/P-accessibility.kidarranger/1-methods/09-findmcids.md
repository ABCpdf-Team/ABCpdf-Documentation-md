---
title: "09-findmcids"
css: "abcpdf-docs.css"
---

|  |  | FindMcids Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Finds all the MCIDs referenced by this structure element and its children. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp FindMcids(this StructureElementElement element, Dictionary> mcids) ``` [Visual Basic] ``` FindMcids(this StructureElementElement element, Dictionary> mcids) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| mcids | The structure to which MCIDs should be added. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Finds all the MCIDs referenced by this structure element and its children. These MCIDs are added to the mcids Dictionary provided. The Dictionary maps Page objects to a HashSet of MCID integer IDs. |  |  | 
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