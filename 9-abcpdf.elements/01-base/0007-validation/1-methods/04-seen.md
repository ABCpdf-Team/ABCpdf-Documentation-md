---
title: "04-seen"
css: "abcpdf-docs.css"
---

|  |  | Seen Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to indicate that a particular RefAtom has been seen. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void Seen(RefAtom refAtom) ``` [Visual Basic] ``` Overridable Function Seen(refAtom As RefAtom) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| refAtom | The RefAtom. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to indicate that a particular RefAtom has been seen. Most of the time the Start method can be used to keep track of which IndirectObjects have been seen. However occasionally a RefAtom may not resolve to an Element that can be validated. For example the Length entry in a StreamElement is a number indicating the number of bytes of data in the stream. In most cases this is a simple number embedded as the value of the Length entry in the dictionary. However some PDFs represent this as a reference to an IndirectObject containing a number. Since it is a reference to a number there is no Element type for it and it will not get validated. For the basic validation process this will not matter since the reference is automatically resolved and a simple number provided. However if you are keeping track of which IndirectObjects have been validated, it is important to know about these cases. You can do so by overriding this function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>