---
title: "getpositionandlength"
css: "abcpdf-docs.css"
---

|  |  | GetPositionAndLength Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the position and length of an operator and the parameters that it takes. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Tuple GetPositionAndLength(IndirectObject owner, ArrayAtom array, int index) ``` [Visual Basic] ``` Sub GetPositionAndLength(owner As IndirectObject, array As ArrayAtom, index As int) As Tuple ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| owner | The owner of the operator. | 
| array | The content stream ArrayAtom. | 
| index | The index of the operator within the array. | 
| return | The position and length within the data. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets the position and length of an operator and the parameters that it takes. The item in the array at the index provided must be an OpAtom or an exception will be raised. The position returned is relative to the complete content stream sequence. To convert this to an offset within a particular stream you can pass the relevant. offset to the GetStreamAndOffset function. |  |  | 
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