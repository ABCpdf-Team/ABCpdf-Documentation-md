---
title: "5-equals"
css: "abcpdf-docs.css"
---

|  |  | Equals Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Test whether the two IndirectObjects are the same. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Equals(IndirectObject other) override bool Equals(object other) bool Equals(IndirectObject other, ComparisonType type) ``` [Visual Basic] ``` Function Equals(other As IndirectObject) As Boolean Overrides Function Equals(other As Object) As Boolean Function Equals(other As IndirectObject, type As ComparisonType) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| other | The object to test against. | 
| return | Whether the objects are equal. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method can be used to determine whether the specified object is equal to the current object. Objects are considered equal if they refer to the same underlying object within the PDF document. So by default this method determines object equality rather than value equality. To perform other types of equality test you can use the overload that accepts a ComparisonType. The comparison type specifies the type of data to compare. The ComparisonType enumeration is a flags type enumeration so the different values can be combined together using bitwise operations. It may take the following values: None (nothing) Object (the underlying PDF object) ID (the ID of the IndirectObject) Atom (the value of the Atom) Data (the data associated with the stream - if this is a stream) Only if all the comparisons are true are the objects said to be equal. |  |  | 
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