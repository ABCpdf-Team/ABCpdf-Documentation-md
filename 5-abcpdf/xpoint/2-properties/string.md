---
title: "string"
css: "abcpdf-docs.css"
---

|  |  | String Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "0 0" | No | The point as a string | 

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
      
| Allows you to access to the point as a string. The format of the string must be "x y". |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code. [C#] ```csharp var pt = new XPoint(); pt.String = "20 10"; Response.Write($"X = {pt.X}"); Response.Write(""); Response.Write($"Y = {pt.Y}"); ``` [Visual Basic] ```vbnet Dim pt As New XPoint() pt.String = "20 10" Response.Write($"X = {pt.X}") Response.Write("") Response.Write($"Y = {pt.Y}") ``` Produces the following output. X = 20 Y = 10 Also see example code in: ABCpdf Advanced Graphics Example, ABCpdf Fields, Markup and Movies Example, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XTransform Invert Function, XTransform Reset Function, XTransform Rotate Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>