---
title: "compressjpx"
css: "abcpdf-docs.css"
---

|  |  | CompressJpx Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Compresses the image using JPEG 2000 compression. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void CompressJpx(int quality) ``` [Visual Basic] `Sub CompressJpx(quality As Integer)` `may throw Exception()` |  |  | 
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
| quality | The quality of compression to use (0 to 100). | 

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
      
| Compresses the image using JPEG 2000 compression. JPEG 2000 compression can be used on RGB, Grayscale or CMYK images. It offers high compression levels for continuous tone images like photographs. However it is a lossy method which means that the quality of the compressed image will not be as good as the uncompressed image. The quality of the compression can range from zero (lowest quality, highest compression) to 100 (lossless quality, lowest compression). A good generic value is 75. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: RecolorOperation Recolor Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>