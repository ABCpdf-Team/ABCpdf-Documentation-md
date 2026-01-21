---
title: "03-processitem"
css: "abcpdf-docs.css"
---

|  |  | ProcessItem Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Process an item in a content stream and update the graphics or text state to reflect the action of the item. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ProcessItem(IndirectObject owner, ArrayAtom contents, string op, int pos) ``` [Visual Basic] ``` Overridable Function ProcessItem(owner As IndirectObject, contents As ArrayAtom, op As string, pos As int) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| owner | The owner of the stream - either a Page or Form XObject. | 
| contents | The contents of the stream as obtained from a call to ArrayAtom.FromContentStream or similar. | 
| op | The name of the operator. For example this might be "cm" or "q". | 
| pos | The index of the operator in the contents array. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Process an item in a content stream and update the graphics or text state to reflect the action of the item. For your own operator processing you will wish to override this function. |  |  | 
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