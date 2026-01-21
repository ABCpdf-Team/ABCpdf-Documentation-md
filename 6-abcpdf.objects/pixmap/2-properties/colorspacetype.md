---
title: "colorspacetype"
css: "abcpdf-docs.css"
---

|  |  | ColorSpaceType Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp ColorSpaceType ``` [Visual Basic] `ColorSpaceType` | n/a | No | The ColorSpace for this image. | 

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
      
| The ColorSpaceType for this image. Referencing this property has a number of advantages over referencing the PixMap.ColorSpace.ColorSpaceType property. Firstly it avoids the possibility that a new ColorSpace object will need to be created. Secondly it takes account of the fact that certain types of PixMap (e.g. ImageMasks) do not have a ColorSpace. In these cases the ColorSpaceType is implicit in the definition of the PixMap and needs to be inferred by the PixMap itself. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>