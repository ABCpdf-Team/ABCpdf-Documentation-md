---
title: "alpha"
css: "abcpdf-docs.css"
---

|  |  | Alpha Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 255 | No | The alpha opacity. | 

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
      
| Allows you to get or set the alpha opacity of the color. Alpha values can range from 0 to 255. Zero indicates fully transparent and 255 indicates fully opaque. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Here we create a PDF document showing how different values of alpha result in different levels of transparency. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(20, 20); doc.FontSize = 300; for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(20, 20) doc.FontSize = 300 Dim i As Integer = 1 While i coloralpha.pdf Also see example code in: SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>