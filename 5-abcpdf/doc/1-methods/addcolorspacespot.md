---
title: "addcolorspacespot"
css: "abcpdf-docs.css"
---

|  |  | AddColorSpaceSpot Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a separation color space to the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddColorSpaceSpot(string name, string color) ``` [Visual Basic]`Function AddColorSpaceSpot(name As String, color As String) As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| name | The name of the color. | 
| color | The display representation of the color. This should be supplied in the same format as the XColor.String uses. | 
| return | The Object ID of the newly added ColorSpace Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a separation color space to the document returning the ID of the newly added object. Separation color spaces allow you to add spot colors or isolate the use of individual colorants. A separation color space represents a particular colorant and allows you to specify the amount of that colorant that is applied. For example you might define a separation color space called Gold with a display representation of CMYK yellow. You might then draw some text with different amounts of Gold. When viewing the output on a standard monitor the display representation of the color would be used. However when printed - using appropriate software and an appropriate printer - the name of the color might be used to select a gold colored ink. The current color space is defined by the ColorSpace property. The current color is defined by the Color property. Because separations represent a single value property you should use single component - grayscale - colors to specify the amount of spot colorant to use. There are two special color spaces: 'All' refers collectively to all colorants on an output device. It can be useful for printing registration marks. 'None' indicates no colorant and will never produce any visible output. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| In this example we define a colorant called Gold and add some text using varying amounts of our colorant. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(20, 20); doc.FontSize = 300; doc.ColorSpace = doc.AddColorSpaceSpot("GOLD", "0 0 100 0"); for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(20, 20) doc.FontSize = 300 doc.ColorSpace = doc.AddColorSpaceSpot("GOLD", "0 0 100 0") Dim i As Integer = 1 While i docaddcolorspacespot.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>