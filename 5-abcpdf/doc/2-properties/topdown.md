---
title: "topdown"
css: "abcpdf-docs.css"
---

|  |  | TopDown Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | The current position of the origin. | 

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
      
| PDF coordinates are measured upwards from the bottom of the document. For some types of layout it can be useful to measure coordinates downwards from the top of the document. By setting this property to true coordinates are assumed to start at the top rather than the bottom of the document. More precisely the origin is assumed to be at the top-left of the current MediaBox. There are a variety of methods you can use to change coordinate systems. Note that transforms operate on the underlying PDF coordinate space rather than any abstraction specified by the Units and TopDown properties. If you are using transforms you will find it easiest to work in the native PDF coordinate space. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code creates a PDF document and adds a grid measured in inches. [C#] ```csharp using var doc = new Doc(); doc.Units = UnitType.Inches; doc.TopDown = true; doc.Width = 1.0 / 8.0; doc.FontSize = 1; doc.Rect.Pin = XRect.Corner.TopLeft; for (int i = 0; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Units = UnitType.Inches doc.TopDown = True doc.Width = 1.0 / 8.0 doc.FontSize = 1 doc.Rect.Pin = XRect.Corner.TopLeft Dim i As Integer = 0 While i doctopdown.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>