---
title: "setdata"
css: "abcpdf-docs.css"
---

|  |  | SetData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the raw binary content of the stream. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetData(byte[] value) void SetData(byte[] value, int index, int count) void SetData(StreamObject source) void SetData(byte[] buffer, bool clearFirst) void SetData(byte[] buffer, int index, int count, bool clearFirst) ``` [Visual Basic] ``` Sub SetData(value() As Byte) Sub SetData(value() As Byte, index As Integer, count As Integer) Sub SetData(source As StreamObject) Sub SetData(buffer() As Byte, clearFirst As bool) Sub SetData(buffer() As Byte, index As int, count As int, clearFirst As bool) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| value | The raw binary content to be assigned to the stream. | 
| index | The index in the array at which copying should start. | 
| count | The number of bytes to copy. | 
| source | The source stream from which to copy the data. | 
| clearFirst | Whether to clear any compression settings before assigning the data bytes. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Set the raw binary content of the stream. Compression settings are unaltered. So if - for example - you have a stream which is Flate compressed you must use SetData with Flate compressed data. For this reason you may wish to call ClearData before using SetData. Using the overload which accepts a StreamObject is equivalent to, but more efficient than, getting the data from the source StreamObject and then using SetData to assign it to this one. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: OpAtom Find Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>