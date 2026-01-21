---
title: "icccmyk"
css: "abcpdf-docs.css"
---

|  |  | IccCmyk Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "standard" | No | The path to the default CMYK ICC color profile. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| A path to the default CMYK ICC color profile. For a device independent conversion both the source and destination color spaces must both have a color profile. They may have a color profile available because one has been embedded in the PDF, or one may be available as a fallback option via the IccCmyk, IccRgb, IccGray and IccOutput properties. If profiles are available for both source and destination, the profile for the source may be used to convert any device CMYK colors to the device independent CIE working color space. From the working space the color can then be converted to the DestinationColorSpace. If either the source or destination do not have a color profile then no accurate conversion is possible and simple mathematical formulas will be used to convert from the source color space to the destination. This property can take a path to an icm file. If this property is set to a file name with no path information, then the system ICC color profile directory will be searched to locate the file. However there are also two special values you can use. If the property takes the value "standard" then a built in default color profile will be used. If the property takes the value "device" then the output is device dependent - no fallback profile is available. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example illustrates how one could convert the first page of a PDF document so all colors and color spaces are in Lab format Any DeviceCMYK color values are run though the CoatedGRACoL2006 ICC color profile for conversion to Lab. We assign 96 to the Type0SampleCount which means that continuous shading functions are converted to Type 0 (sample based) functions with 96 samples. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/SpaceShuttlePage6.pdf")); var cs = new ColorSpace(doc.ObjectSoup, ColorSpaceType.Lab); using (var op = new RecolorOperation()) { op.DestinationColorSpace = cs; op.IccCmyk = Server.MapPath("../Rez/EuroscaleCoated.icc"); op.Type0SampleCount = 96; op.RenderingIntent = RenderingIntent.Perceptual; op.Recolor((Page)doc.ObjectSoup[doc.Page]); } doc.Save(Server.MapPath("RecolorToLab.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/SpaceShuttlePage6.pdf")) Dim cs As New ColorSpace(doc.ObjectSoup, ColorSpaceType.Lab) Using op = New RecolorOperation() op.DestinationColorSpace = cs op.IccCmyk = Server.MapPath("../Rez/EuroscaleCoated.icc") op.Type0SampleCount = 96 op.RenderingIntent = RenderingIntent.Perceptual op.Recolor(DirectCast(doc.ObjectSoup(doc.Page), Page)) End Using doc.Save(Server.MapPath("RecolorToLab.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>