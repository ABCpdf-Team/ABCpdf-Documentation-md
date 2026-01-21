---
title: "imagemask"
css: "abcpdf-docs.css"
---

|  |  | ImageMask Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | n/a | No | Whether this image is a one bit image mask. | 

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
      
| Whether this image is a one bit image mask. Setting this value to true will change the PixMap to a mask. There are certain restrictions on masks which must be checked before this is done. Namely, if the mask has a Mask of its own, or if the BitsPerComponent is not one then an exception will be raised. Changing the value to false will remove the mask entry from this PixMap and convert the color space to grayscale. It is your responsibility to detach this object from any PixMaps which may be using it as a mask. |  |  | 
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