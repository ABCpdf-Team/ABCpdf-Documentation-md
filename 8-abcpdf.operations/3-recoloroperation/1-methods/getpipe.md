---
title: "getpipe"
css: "abcpdf-docs.css"
---

|  |  | GetPipe Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets a color conversion Pipe which may be used to map colors from one color space to another. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp RecolorOperation.Pipe GetPipe(Page page, Atom source) ``` [Visual Basic] ``` Function GetPipe(page As Page, source As Atom) As RecolorOperation.Pipe ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| page | The page for which the pipe is needed. | 
| source | The source color space atom. | 
| returns | A Pipe which can be used for converting colors. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets a color conversion Pipe which may be used to map colors from one color space to another. The Pipe maps from the provided color space source in the context of the provided page, to the DestinationColorSpace and RenderingIntent of the RecolorOperation. Pipes are owned by the RecolorOperation which means that repeated Pipe requests will use cached Pipes rather than recreating the same conversion repeatedly. While this greatly increases the efficiency of conversion, it does also mean that at the point at which the RecolorOperation is disposed of, all owned Pipes will also be disposed of. So if you attempt to use a Pipe after your RecolorOperation has been disposed of, an exception will be raised. |  |  | 
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