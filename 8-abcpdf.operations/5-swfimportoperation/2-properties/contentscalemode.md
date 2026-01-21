---
title: "contentscalemode"
css: "abcpdf-docs.css"
---

|  |  | ContentScaleMode Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp ContentScaleMode? ``` [Visual Basic]`Nullable(Of ContentScaleMode)` | ExactFit | No | Gets or sets the content scale mode. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property specifies the scale mode of the content in the target rectangle. It can take any of the following values: ShowAll – make the content the biggest and completely within the area while keeping the aspect ratio. NoBorder – make the content the smallest and covering the entire area while keeping the aspect ratio. ExactFit – scale the content possibly with distortion to fit the entire area. NoScale – no scaling. If it is null, the value of the ActionScript property Stage.scaleMode is used. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the ProcessingInfo.FrameNumber property. Also see example code in: ProcessingInfo FrameNumber Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>