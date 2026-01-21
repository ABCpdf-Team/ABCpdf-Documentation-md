---
title: "string"
css: "abcpdf-docs.css"
---

|  |  | String Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "1 0 0 1 0 0" | No | The transform as a string. | 

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
      
| Allows you access to the transform as a string. The format of the string must be "m11 m12 m21 m22 mX mY". To transform a point (x, y) to another point (x', y'), the following formula is used: ``` x' = (x * m11) + (y * m21) + mX y' = (x * m12) + (y * m22) + mY ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: Page GetBitmap Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>