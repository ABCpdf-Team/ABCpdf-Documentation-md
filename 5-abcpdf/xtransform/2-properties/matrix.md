---
title: "matrix"
css: "abcpdf-docs.css"
---

|  |  | Matrix Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Matrix ``` [Visual Basic] `Matrix` | n/a | No | The transform as a System.Drawing.Drawing2D Matrix. | 

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
      
| The transform as a System.Drawing.Drawing2D Matrix. This matrix type holds element values as single precision floating point values so it is is less accurate than the underlying XTransform. Windows coordinates are measured in distances from the top left of the drawing surface while PDF coordinates are measured from the bottom left. Remember that transforms operate on the underlying PDF coordinates rather than on any Windows coordinates. So by specifying a rotation around the origin you are specifying a rotation anchored at the bottom left of the document page. |  |  | 
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