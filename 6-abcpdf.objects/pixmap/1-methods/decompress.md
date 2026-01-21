---
title: "decompress"
css: "abcpdf-docs.css"
---

|  |  | Decompress Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Decompress the data in the stream using on-the-fly resizing |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Decompress(int width, int height) ``` [Visual Basic] ``` Function Decompress(width As Integer, height As Integer) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| width | The desired final width. | 
| height | The desired final height | 
| return | Whether the data was decompressed correctly. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Decompress the data in the stream using on-the-fly resizing of the image. This type of scaling is fast and memory efficient but may change the depth of the image. Only some compression types support on-the-fly resizing. As such you should always check the dimensions of the image after calling this method. Do not assume that simply because the image has decompressed correctly that it has also been resized. |  |  | 
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