---
title: "getrange"
css: "abcpdf-docs.css"
---

|  |  | GetRange Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Creates a shallow copy of a range of elements in the source array |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp ArrayAtom GetRange(int index, int count) ``` [Visual Basic] ``` Function GetRange(index As Integer, count As Integer) As ArrayAtom ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| index | The zero-based index specifying the first element. | 
| count | The number of elements to be selected. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Creates a shallow copy of a range of elements in the source array. If the index is equal to the Count then the elements are added to the end of the array. If the index or count is invalid then an exception will be raised. |  |  | 
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