---
title: "realize"
css: "abcpdf-docs.css"
---

|  |  | Realize Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Converts the image to component color. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void Realize() ``` [Visual Basic] `Sub Realize()` `may throw Exception()` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| none |  | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Converts the image from indexed color to component color. The process of converting an indexed color image into a component color image, will result in any chromakeys being converted to masks and the elimination of any decode arrays. The Indexed color space is used for palletized color. Each item in the palette is defined in terms of a base color space such as DeviceRGB. Palettes can hold up to 256 entries. After an indexed color image has been realized it is no longer compressed. You may wish to compress it using the StreamObject.Compress method. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the Resize function. Also see example code in: PixMap Resize Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>