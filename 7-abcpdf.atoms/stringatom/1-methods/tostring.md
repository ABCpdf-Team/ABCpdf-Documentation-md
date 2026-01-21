---
title: "tostring"
css: "abcpdf-docs.css"
---

|  |  | ToString Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The string representation of the StringAtom as it would appear in a PDF. |  |  | 

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
      
| This function derives the content of the object as it will be inserted into the final PDF document. There are many ways in which a string may be represented. The format string allows more control over how this is done. The following options may be used in combination. l - literal format with unusual characters escaped in octal x - hexadecimal format with all characters represented in hex lx - best choice literal or hexadecimal format depending on the content of the string b1 - allow the string to be broken over multiple lines b0 - do not allow the string to be broken over multiple lines r1 - allow random elements when applying a crypt filter r0 - do not allow random elements when applying a crypt filter If format options are not specified then ABCpdf will select a sensible set depending on context. |  |  | 
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