---
title: "03-insert"
css: "abcpdf-docs.css"
---

|  |  | Insert Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Inserts an Element into the array at the specified position. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void Insert(int index, T value) ``` [Visual Basic] ``` Overridable Function Insert(index As int, value As T) As void ``` `ArgumentOutOfRangeException: Thrown if the index provided is not valid. NullReferenceException: Thrown if an attempt is made to insert a null value in a non-Nullable array.` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| index | The zero-based index at which value should be inserted. | 
| value | The Element to insert into the array. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Inserts an Element into the array at the specified position. If the index equals the number of items in the array then the Element is appended to the end. Most ArrayElements cannot hold null values in a meaningful way. So in general, if you provide a null value this will result in an exception being raised. Occasionally it is appropriate for ArrayElements to hold null values represented as NullAtoms. You can indicate this is acceptable, by setting the Nullable property. |  |  | 
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