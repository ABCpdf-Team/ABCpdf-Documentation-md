---
title: "2-copyto"
css: "abcpdf-docs.css"
---

|  |  | CopyTo Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Copy the objects in this subset to a new soup while preserving the relationships between the items in the selection. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void CopyTo(ObjectSoup soup) ``` [Visual Basic] ``` Sub CopyTo(soup As ObjectSoup) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| soup | The destination soup. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Copy the objects in this subset to a new soup while preserving the relationships between the items in the selection. Each IndirectObject in the selection has a unique ID. However the destination soup may already contain items with this ID. For this reason the process of copying the objects requires a remapping of old IDs to new ones in the destination soup. Some remap entries may already have been created during addition as the entries in the RemapTypes property get applied. However most will be created at the point that the CopyTo method is called. The remap table is accessible via the RemapIDs property. |  |  | 
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