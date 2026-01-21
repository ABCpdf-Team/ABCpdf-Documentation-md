---
title: "streamposition"
css: "abcpdf-docs.css"
---

|  |  | StreamPosition Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp long? ``` [Visual Basic]`Nullable(Of Long)` | n/a | Yes | Gets or Sets the stream position of the source object, if applicable. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The value of this property when the Operation.ProcessingObject event is generated depends on the operation. This property holds the position in the PDF stream. Set this value to null to end the processing of the current stream. See the RenderOperation.Save method. |  |  | 
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