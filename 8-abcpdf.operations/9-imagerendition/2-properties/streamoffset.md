---
title: "streamoffset"
css: "abcpdf-docs.css"
---

|  |  | StreamOffset Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Int32` | n/a | Yes | The offset within the uncompressed StreamObject to the start of the drawing operation that contains this image draw operation. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The offset within the uncompressed StreamObject to the start of the drawing operation that contains this image draw operation. The combination of the StreamObject, StreamOffset and StreamLength allows you to precisely locate the image draw command sequence in the PDF content stream. This can then be used to modify or delete this particular command. |  |  | 
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