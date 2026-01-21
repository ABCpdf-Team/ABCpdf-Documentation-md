---
title: "2-copyto"
css: "abcpdf-docs.css"
---

|  |  | CopyTo Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Copies the Atoms into an array. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void CopyTo(Atom[] array, int index) void CopyTo(KeyValuePairAtom>[] array, int index) ``` [Visual Basic] ``` Sub CopyTo(array As Atom(), index As Integer) Sub CopyTo(array As KeyValuePair(Of String, Atom)(), index As Integer) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| array | The array that is the destination for the elements. | 
| index | The zero-based index in array at which copying begins. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Copies the elements of the dictionary to an array starting at a particular array index. The array must be one-dimensional and have zero-based indexing. The implementation of ICollection.CopyTo copies KeyValuePair values to the array if the element type of the array is compatible. Otherwise, it copies DictionaryEntry values to the array. |  |  | 
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