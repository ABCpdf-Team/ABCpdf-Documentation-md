---
title: "docnumber"
css: "abcpdf-docs.css"
---

|  |  | DocNumber Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int? ``` [Visual Basic]`Nullable(Of Integer)` | n/a | No | Gets or sets the document number of the source document being/to be processed. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The value of this property when the Operation.ProcessingObject event is generated depends on the operation. The event handler should change this value when a processing sequence other than the default is desired. Set this value to null to end the processing of the current set of documents. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the XpsImportOperation.Import method. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>