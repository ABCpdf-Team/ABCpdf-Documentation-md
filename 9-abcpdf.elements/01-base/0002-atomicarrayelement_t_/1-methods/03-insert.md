---
title: "03-insert"
css: "abcpdf-docs.css"
---

|  |  | Insert Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Inserts an item into the array at the specified position. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void Insert(int index, T value) ``` [Visual Basic] ``` Overridable Function Insert(index As int, value As T) As void ``` `ArgumentOutOfRangeException: Thrown if the index provided is not valid.` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| index | The zero-based index at which the value should be inserted. | 
| value | The items to insert into the array. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Inserts an item into the array at the specified position. If the index equals the number of items in the array then the items is appended to the end. If the type indicated is string then a null string will be interpreted as an empty string. If the type indicated is a double? then a null value will be interpreted as a NullAtom. All other types are non-nullable. |  |  | 
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