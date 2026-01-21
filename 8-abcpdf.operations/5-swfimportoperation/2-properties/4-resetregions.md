---
title: "4-resetregions"
css: "abcpdf-docs.css"
---

|  |  | ResetRegions Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic]`Boolean` | true | No | Gets or sets a value that indicates whether BackgroundRegion and ClipRegion are reset when the Operation.ProcessingObject event of ProcessingSourceType.MultiFrameImage or of ProcessingSourceType.ImageFrame is generated. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Indicates whether the background and clip regions should be reset to the frame bounds each time a new frame is about to be imported. The regions are set as if XRect.SetRect is called with the X, Y, Width, and Height properties of the ProcessingInfo. Set this property to false when you want the regions not to be reset when the Operation.ProcessingObject event of ProcessingSourceType.MultiFrameImage or of ProcessingSourceType.ImageFrame is generated. |  |  | 
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