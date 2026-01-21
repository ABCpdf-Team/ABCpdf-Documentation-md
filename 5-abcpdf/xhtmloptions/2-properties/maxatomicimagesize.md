---
title: "maxatomicimagesize"
css: "abcpdf-docs.css"
---

|  |  | MaxAtomicImageSize Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 480 | No | The maximum size at which an image may be regarded as unbreakable. | 

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
      
| ABCpdf generally regards images as atomic - unbreakable over more than one page. However when an image reaches a certain size it's impossible to stop the image being broken. To try do so would result in unacceptable gaps in the content. So the assumption that the image is atomic has to be disregarded. This property reflects the height (in pixels) at which images will be redefined as non-atomic. |  |  | 
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