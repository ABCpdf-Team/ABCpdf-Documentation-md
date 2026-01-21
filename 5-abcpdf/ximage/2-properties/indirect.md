---
title: "indirect"
css: "abcpdf-docs.css"
---

|  |  | Indirect Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | See description. | Yes | Whether the image will be added using indirect mode. | 

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
      
| This property tells you whether the image will be added using indirect mode. The name of this property is related to how the XImage object used to work and so it is no longer very meaningful. So, ignoring the name, the core function of this property is is to tell you whether you can use the Selection property and SetMask method. This property is false for EPS and PS image types. It is false for EMF or WMF files imported using the EmfVector ReadModule. In all other cases it is true. |  |  | 
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