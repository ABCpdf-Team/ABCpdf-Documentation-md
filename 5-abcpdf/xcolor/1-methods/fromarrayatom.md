---
title: "fromarrayatom"
css: "abcpdf-docs.css"
---

|  |  | FromArrayAtom Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create an XColor from an ArrayAtom of NumAtoms containing PDF color values. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static XColor FromArrayAtom(ArrayAtom array) ``` [Visual Basic] ``` Shared Function FromArrayAtom(array As ArrayAtom) As XColor ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| array | The ArrayAtom containing the components of the color. | 
| return | The resulting XColor. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create an XColor from an ArrayAtom of NumAtoms containing PDF color values. There may be only one, three or four items in the ArrayAtom. The number of items is used to select between Grayscale, RGB or CMYK color spaces respectively. The values expected are PDF color values so all the atoms in the ArrayAtom must be NumAtoms with a value between zero and one, each representing a component of the color. If these conditions are not met then an exception will be raised. |  |  | 
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