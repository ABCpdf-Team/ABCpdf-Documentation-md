---
title: "getstreamandoffset"
css: "abcpdf-docs.css"
---

|  |  | GetStreamAndOffset Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Finds the location of an operator in a set of streams. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Tuple GetStreamAndOffset((IndirectObject owner, int offset, int length) ``` [Visual Basic] ``` Sub GetStreamAndOffset(owner As IndirectObject, offset As int, length As int) As Tuple ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| owner | The owner of the content sequence. | 
| offset | The offset of the start of the token. | 
| length | The length of the token. | 
| return | A pair representing the containing StreamObject and the offset to the start of the token. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Finds the location of an operator in a set of streams. Given the offset and length of a token (typically an operator), this function determines the StreamObject in which it is located and the offset within that StreamObject. If the offset cannot be found then an exception will be raised. If the operator is split over two StreamObjects then an exception is thrown. The PDF specification prohibits a token being split in this way so this should not happen. |  |  | 
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