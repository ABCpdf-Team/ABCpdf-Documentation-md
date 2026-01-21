---
title: "6-gethashcode"
css: "abcpdf-docs.css"
---

|  |  | GetHashCode Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A hash code for the IndirectObject. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp override int GetHashCode() int GetHashCode(ComparisonType type) ``` [Visual Basic] ``` Overrides Function GetHashCode() As Integer Function GetHashCode(type As ComparisonType) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| type | The elements to use in the hash code. | 
| return | The returned hash code. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Derives a hash code suitable for use in hashing algorithms and data structures like hash tables. The default hash code is derived from the underlying object within the PDF document. In some situations you may wish to derive a hash code from just some aspects of the IndirectObject. You can do this using the overload which takes a ComparisonType argument. The ComparisonType enumeration is a flags type enumeration so the different values can be combined together using bitwise operations. It may take the following values: None (nothing) Object (the underlying PDF object) ID (the ID of the IndirectObject) Atom (the value of the Atom) Data (the data associated with the stream - if this is a stream) The hash code can be made up of a variety of parts of the indirect object combined together. The ID and the Atom hash codes are derived from the value of the ID and Atom respectively. The Data hash code is made from a sample of the compressed data contained in the stream. So two StreamObjects, compressed differently, will return different hash codes even if the uncompressed data is identical. The data sample is kept small - in the order of a few hundred bytes - to ensure a fast response even for very large streams. |  |  | 
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