---
title: "5-gethashcode"
css: "abcpdf-docs.css"
---

|  |  | GetHashCode Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A hash code for the Atom. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp override int GetHashCode() int GetHashCode(ComparisonType type) ``` [Visual Basic] ``` Overrides Function GetHashCode() As Integer Function GetHashCode(type as ComparisonType) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| type | The type of data to hash. | 
| return | The returned hash code. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Derives a hash code suitable for use in hashing algorithms and data structures like hash tables. The override taking a ComparisonType allows you to choose between different ways of evaluating the hash. The enum is flags based so you can combine different options. The ComparisonType provides the following options: None - Hash a constant value. Object - Hash the object - analogous to object equality. Atom - Hash the value - analogous to value equality. |  |  | 
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