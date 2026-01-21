---
title: "getparameters"
css: "abcpdf-docs.css"
---

|  |  | GetParameters Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the parameters associated with the OpAtom at the specified index and validates that the atoms are of the correct type |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Atom[] GetParameters(ArrayAtom array, int index) ``` [Visual Basic] ``` Function GetParameters(array As ArrayAtom, index As Integer) As Atom() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| array | The array in which the OpAtom is found. | 
| index | The index to the OpAtom. | 
| return | The parameters. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets the parameters associated with the OpAtom at the specified index and validates that the atoms are of the correct type. Because the arguments are validated and the types are checked so you can rely on the fact that the returned array contains a valid number of Atoms of the correct types. Only the top level atoms are checked. So for example, the TJ operator takes an ArrayAtom consisting of NumAtoms and StringAtoms. This function will ensure that there is one ArrayAtom available as a parameter. However it will not ensure that all items inside the array are NumAtoms or StringAtoms. Also resource lookups are not done so, for example, it is not checked that a font name actually exists in the font resource dictionary. If the operator takes no parameters a zero length array will be returned. If the operator parameters are incorrect or if the operator is not recognized then the return value will be null. In this unusual situation you may wish to set the OpAtom.Text to white space to remove the invalid operator from the content stream. While this does not fix the underlying problem, it will at least prevent applications like Acrobat from reporting an error. |  |  | 
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