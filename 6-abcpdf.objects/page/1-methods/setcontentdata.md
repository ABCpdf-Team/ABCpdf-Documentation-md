---
title: "setcontentdata"
css: "abcpdf-docs.css"
---

|  |  | SetContentData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets the content data for the page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp StreamObject SetContentData(byte[] buffer, bool compress) StreamObject SetContentData(byte[] buffer, int index, int count, bool compress) ``` [Visual Basic] ``` Sub SetContentData(buffer() As Byte, compress As bool) As StreamObject Sub SetContentData(buffer() As Byte, index As int, count As int, compress As bool) As StreamObject ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| buffer | The bytes containing the data to be set. | 
| compress | Whether the new stream should be Flate compressed. | 
| index | The byte offset in buffer, at which to begin copying bytes to the page contents. The default is zero. | 
| count | The number of bytes to be written to the page contents. The default is the buffer.Length. | 
| return | The stream containing the data. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Sets the content data for the page. You can specify a subset of the bytes in the array as the data for the content stream. If the data for the current page is the same as that provided then nothing will be done and the existing stream will be returned. |  |  | 
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