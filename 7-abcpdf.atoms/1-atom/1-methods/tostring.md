---
title: "tostring"
css: "abcpdf-docs.css"
---

|  |  | ToString Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The string representation of the Atom as it would appear in a PDF. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp override string ToString() string ToString(string format) ``` [Visual Basic] ``` Overrides Function ToString() As String Function ToString(format As String) As String ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| format | The format which should be used for the conversion. | 
| return | The string representation of the object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function derives the content of the object as it will be inserted into the final PDF document. Note that the the string value of an object may be large and it may contain unusual characters. The StringAtom is the only Atom type to support different format strings. Other Atom types will ignore them. |  |  | 
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