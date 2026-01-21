---
title: "2-processedobject"
css: "abcpdf-docs.css"
---

|  |  | ProcessedObject Event |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Occurs just after an IndirectObject has been processed. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp event ProcessedObjectEventHandler ProcessedObject; delegate void ProcessedObjectEventHandler(object sender, ProcessedObjectEventArgs e); ``` [Visual Basic] ``` Event ProcessedObject As ProcessedObjectEventHandler Delegate Sub ProcessedObjectEventHandler(sender As Object, e As ProcessedObjectEventArgs); ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| sender | The Operation firing the event. | 
| e | The ProcessedObjectEventArgs used to report back the status of the operation. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Typically you handle the ProcessedObject event in order to post-process an IndirectObject. To associate the event with your event handle add an instance of the ProcessedObjectEventHandler delegate to the event. The event handler will be called whenever the event occurs. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the RecolorOperation.Recolor method. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>