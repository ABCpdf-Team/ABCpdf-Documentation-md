---
title: "alternatecolorspacetype"
css: "abcpdf-docs.css"
---

|  |  | AlternateColorSpaceType Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp ColorSpaceType ``` [Visual Basic] `ColorSpaceType` | n/a | Yes | The alternate color space for this ICC color profile | 

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
      
| The alternate color space for this ICC color profile. The alternate color space generally indicates the base color space type such as DeviceRGB or DeviceCMYK. This is useful to know if you are attempting to find out the core type of color space referenced by an ICC color profile. In the situation that no alternate color space is available, one can be generated using the UpdateProfile function. |  |  | 
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