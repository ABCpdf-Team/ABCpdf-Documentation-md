---
title: "dotsperinch"
css: "abcpdf-docs.css"
---

|  |  | DotsPerInch Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 72.0 | No | The output resolution in dots per inch (DPI). | 

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
      
| This property determines the resolution of the output image. Because PDF documents specify distances in physical units (typically points) a resolution unit is needed to convert these physical units to pixel based units. For example a document 612 points wide rendered at 144 DPI will result in an output image 1224 pixels wide. Changing this property will change the values of both the DotsPerInchX and DotsPerInchY properties. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the DefaultHalftone property. Also see example code in: ABCpdf PDF Rendering Example, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering ColorSpace Property, XRendering DefaultHalftone Property, XRendering IccCmyk Property, XRendering Overprint Property, XRendering SaveQuality Property, Page GetBitmap Function, Page Thumbnail Property, PixMap GetBitmap Function, RenderOperation Save Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>