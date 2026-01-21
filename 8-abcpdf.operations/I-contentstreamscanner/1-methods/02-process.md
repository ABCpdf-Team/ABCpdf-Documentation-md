---
title: "02-process"
css: "abcpdf-docs.css"
---

|  |  | Process Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Process a content stream keeping track of state. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void Process(IndirectObject owner, ArrayAtom contents) Process(IndirectObject owner, ArrayAtom contents, IList> ops) ``` [Visual Basic] ``` Overridable Function Process(owner As IndirectObject, contents As ArrayAtom) As void Process(IndirectObject owner, ArrayAtom contents, IList> ops) ``` |  |  | 
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
| ops | The operators to process as obtained from a call to OpAtom.Find or similar. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Process a content stream keeping track of state. In general you will not need to do this but you can assign custom graphics State settings prior to calling this function. At completion this function will assign a new graphics state stack ready for the next call. |  |  | 
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