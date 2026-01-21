---
title: "bitsperchannel"
css: "abcpdf-docs.css"
---

|  |  | BitsPerChannel Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 8 | No | The output bits per color channel. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </tbody></table>
    </td>
  </tr>
  <tr> 
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property determines the precision of the output color channels. The value is specified in terms of the number of bits used to represent each channel of color. This can be 1, 8 or 16. All color spaces support 8 and 16 bits per channel. Only the Gray color space supports 1 bit per channel - black and white. For details of valid combinations see the ColorSpace property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the DefaultHalftone property. Also see example code in: XRendering DefaultHalftone Property, XRendering SaveCompression Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</tbody></table>