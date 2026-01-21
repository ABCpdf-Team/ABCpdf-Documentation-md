---
title: "3-equals"
css: "abcpdf-docs.css"
---

|  |  | Equals Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Test whether the two Atoms are the same. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Equals(Atom other) override bool Equals(object test) bool Equals(Atom other, ComparisonType type) ``` [Visual Basic] ``` Function Equals(other As Atom) As Boolean Overrides Function Equals(test As Object) As Boolean Function Equals(other As Atom, type as ComparisonType) As Boolean ``` |  |  | 
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
| type | The type of comparison to perform. | 
| return | Whether the objects are equal. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method can be used to determine whether the specified object is equal to the current object. Objects are considered equal if they have the same content - so this method determines value equality rather than object equality. The function taking an object is required as part of the .NET framework, it performs exactly the same task as the function taking an Atom. The override taking a ComparisonType allows you to choose between different ways of evaluating equality. The enum is flags based so you can combine different options. Only if all options evaluate to true will true be returned. The ComparisonType provides the following options: None - Equal as long as the other atom is not null. Object - Equal if the atoms are object equal. Atom - Equal if the atoms are value equal. |  |  | 
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