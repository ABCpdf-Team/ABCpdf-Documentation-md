---
title: "string"
css: "abcpdf-docs.css"
---

|  |  | String Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "0 0 0" | No | The color as a string. | 

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
      
| Allows you access to the color as a string. If the color is in the RGB color space then the string contains three values representing the Red, Green and Blue levels. For example "100 150 200". If the color is in the CMYK color space then the string contains four values representing the Cyan, Magenta, Yellow and Black levels. For example "30 60 90 10". If the color is in the Grayscale color space then the string contains one value representing the Gray level. For example "150". You can use the ColorSpace property to find the current color space for the color. Alpha values can be indicated by prepending an 'a' to an extra component. For example "30 60 90 a120" would indicate an RGB value with an alpha value of 120. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. Also see example code in: ABCpdf Deletion Example, ABCpdf Headers and Footers Example, ABCpdf eForm Placeholder Example, ABCpdf Advanced Graphics Example, Doc AddArc Function, Doc AddColorSpaceFile Function, Doc AddImageBitmap Function, Doc AddImageObject Function, Doc AddLine Function, Doc AddOval Function, Doc AddPie Function, Doc AddPoly Function, Doc Read Function, Doc RemapPages Method, Doc Color Property, Doc Options Property, XHtmlOptions GetTagRects Function, XHtmlOptions HideBackground Property, XHtmlOptions HtmlCallback Property, XImage SetMask Function, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering IccCmyk Property, XRendering SaveAlpha Property, XTransform Magnify Function, XTransform Skew Function, XTransform Translate Function, Page GetBitmap Function, PixMap SetChromakey Function, SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>