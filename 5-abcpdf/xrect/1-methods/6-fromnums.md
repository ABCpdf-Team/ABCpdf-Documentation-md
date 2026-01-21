---
title: "6-fromnums"
css: "abcpdf-docs.css"
---

|  |  | FromNums Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create an XRect from an array or list of four numbers. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static XRect FromNums(double[] array) static XRect FromNums(IList list) ``` [Visual Basic] ``` Shared Function FromNums(array As Double()) As XRect Shared Function FromNums(list As IList(Of Double)) As XRect ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| array | An array containing four doubles. | 
| list | An IList containing four doubles. | 
| return | The newly created XRect object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create an XRect from an array or list of four numbers. Such arrays typically contain lower left x and y coordinates followed by upper right x and y. However this is a convention and any two diagonally opposite points are acceptable. If the array is null or does not contain four items then the return will be null. |  |  | 
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