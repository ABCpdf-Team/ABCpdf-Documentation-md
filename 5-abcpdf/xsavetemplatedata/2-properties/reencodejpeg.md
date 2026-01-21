---
title: "reencodejpeg"
css: "abcpdf-docs.css"
---

|  |  | ReencodeJpeg Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether JPEG images are re-encoded in JPEG. | 

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
      
| This property is effectual where both the source and the destination formats are JPEG. It specifies whether JPEG encoding occurs. When it is false, the source is directly used as the output without re-encoding. When it is true, the source is re-encoded in JPEG. Reencoding allows a JPEG image to use a different quality level. However, reencoding a JPEG image at the same/a higher quality level does not improve the image quality and may degrade it. |  |  | 
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