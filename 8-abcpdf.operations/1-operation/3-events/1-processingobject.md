---
title: "1-processingobject"
css: "abcpdf-docs.css"
---

|  |  | ProcessingObject Event |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Occurs just before an IndirectObject is processed. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp event ProcessingObjectEventHandler ProcessingObject; delegate void ProcessingObjectEventHandler(object sender, ProcessingObjectEventArgs e); ``` [Visual Basic] ``` Event ProcessingObject As ProcessingObjectEventHandler Delegate Sub ProcessingObjectEventHandler(sender As Object, e As ProcessingObjectEventArgs); ``` |  |  | 
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
| e | The ProcessingObjectEventArgs used to control the operation. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Typically you handle the ProcessingObject event in order to determine properties about an IndirectObject before processing. Because the handler passes an EventArgs class which inherits from CancelEventArgs you can also choose to cancel the operation on the IndirectObject. To associate the event with your event handle add an instance of the ProcessingObjectEventHandler delegate to the event. The event handler will be called whenever the event occurs. |  |  | 
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