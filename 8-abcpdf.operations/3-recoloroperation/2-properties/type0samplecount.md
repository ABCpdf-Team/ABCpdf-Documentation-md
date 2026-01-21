---
title: "type0samplecount"
css: "abcpdf-docs.css"
---

|  |  | Type0SampleCount Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Type0SampleCount ``` [Visual Basic]`Type0SampleCount` | 64 | No | Gets or sets the number of Type 0 function samples to generate (between 64 and 1000). | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The default number of Type 0 sample values to generate when converting from a Type 2 to a Type 0 function. When a colorspace that uses a Type 2 function is converted to a new colorspace, that new colorspace is sampled to create a replacement Type 0 function. Many times the default number of samples is adequate, but occasionally one needs more samples to eliminate the subtle banding effect encountered during shades, etc. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: RecolorOperation IccCmyk Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>