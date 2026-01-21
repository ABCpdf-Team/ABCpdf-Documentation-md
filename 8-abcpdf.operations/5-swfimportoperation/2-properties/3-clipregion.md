---
title: "3-clipregion"
css: "abcpdf-docs.css"
---

|  |  | ClipRegion Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp XRect ``` [Visual Basic]`XRect` | null | No | Gets or sets the clip rectangle. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The clip region (in twips) is where the frame foreground is drawn. Set this property to change the extent or location of the frame foreground. If the foreground extends outside of this region, it will be clipped. The clip region is set to the frame bounds/stage size if ResetRegions is true. If it is null (and not set to non-null because of ResetRegions), the content is not clipped. |  |  | 
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