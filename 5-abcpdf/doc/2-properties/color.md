---
title: "color"
css: "abcpdf-docs.css"
---

|  |  | Color Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp XColor ``` [Visual Basic] `XColor` | Black | No | The current drawing and filling color. | 

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
      
| The color used for drawing. This property determines the color used for drawing lines, shapes, filled shapes and text. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code creates a PDF document with a red background. [C#] ```csharp using var doc = new Doc(); doc.Color.String = "255 0 0"; doc.FillRect(); doc.Save(Server.MapPath("doccolor.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Color.String = "255 0 0" doc.FillRect() doc.Save(Server.MapPath("doccolor.pdf")) End Using ``` doccolor.pdfAlso see example code in: ABCpdf Deletion Example, ABCpdf Headers and Footers Example, ABCpdf eForm Placeholder Example, ABCpdf Advanced Graphics Example, Doc AddArc Function, Doc AddColorSpaceFile Function, Doc AddColorSpaceSpot Function, Doc AddImageBitmap Function, Doc AddImageObject Function, Doc AddLine Function, Doc AddOval Function, Doc AddPie Function, Doc AddPoly Function, Doc AddXObject Function, Doc FillRect Function, Doc Read Function, Doc RemapPages Method, Doc Options Property, Doc String Property, XColor Alpha Property, XColor Components Property, XHtmlOptions GetTagRects Function, XHtmlOptions HideBackground Property, XHtmlOptions HtmlCallback Property, XImage SetMask Function, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering IccCmyk Property, XRendering SaveAlpha Property, XTransform Magnify Function, XTransform Skew Function, XTransform Translate Function, ColorSpace Gamma Property, ColorSpace WhitePoint Property, Page GetBitmap Function, PixMap SetChromakey Function, SwfImportOperation Import Function, ImageOperation GetImageProperties Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>