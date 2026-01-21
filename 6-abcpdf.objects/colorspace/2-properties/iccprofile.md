---
title: "iccprofile"
css: "abcpdf-docs.css"
---

|  |  | IccProfile Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp IccProfile ``` [Visual Basic] `IccProfile` | n/a | No | Any ICC Color Profile associated with this color space. | 

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
      
| Any IccProfile describing an ICC Color Profile associated with this color space. Querying the value of this property will never raise an exception. Assigning a new value to this property automatically results in the IccProfile being decompressed, validated, recompressed and (if it is not already there) added to the same ObjectSoup as the ColorSpace. The ColorSpaceType and Components properties will change to reflect the color space of the new profile. An exception will be thrown if the assignation is not possible. This may happen if the ColorSpace is not in an ObjectSoup or if the IccProfile is not valid. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the PixMap.Recolor function. Also see example code in: PixMap Recolor Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>