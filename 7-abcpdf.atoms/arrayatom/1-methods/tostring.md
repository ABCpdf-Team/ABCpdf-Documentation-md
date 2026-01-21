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
      
| This function derives the content of the object as it will be inserted into the final PDF document. There are many ways in which a string may be represented. The format string allows more control over how this is done. The following options may be used in combination. nXX - the number of items per line where XX is the number required If format options are not specified then ABCpdf will select a sensible set depending on context. The number of items per line, determines how many array items will be written on one line. If the number is less than or equal to zero then ABCpdf will dynamically determine an appropriate number of items to be written. Note that items may themselves be ArrayAtom or DictAtom so they may contain their own line breaks. |  |  | 
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