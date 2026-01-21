---
title: "insertrange"
css: "abcpdf-docs.css"
---

|  |  | InsertRange Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Inserts the elements in the supplied array into this array at the specified index |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void InsertRange(int index, ArrayAtom array) ``` [Visual Basic] ``` Sub InsertRange(index As Integer, array As ArrayAtom) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| index | The zero-based index at which the new elements should be inserted. | 
| array | The array whose elements should be inserted. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Inserts the elements in the supplied array into this array at the specified index. If the index is equal to the Count then the elements are added to the end of the array. If the supplied array is null or the index is invalid then an exception will be raised. |  |  | 
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