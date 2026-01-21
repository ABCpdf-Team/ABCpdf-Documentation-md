---
title: "01-elements"
css: "abcpdf-docs.css"
---

|  |  | Elements Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | A rectangle consists of an array of four values - two pairs of pairs. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| A rectangle consists of an array of four values - two pairs of pairs. The first pair represent the x and y coordinates of the lower left of the rectangle,. the second pair represent the x and y coordinates of the upper right of the rectangle. So [lx, ly, ux, uy]. Although the pairs conventially represent the lower left and upper right corners, it is in fact legal to represent any diagaonally opposed corners and. PDF applications will automatically normalize these when they are found. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>