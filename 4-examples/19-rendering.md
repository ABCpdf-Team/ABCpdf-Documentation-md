---
title: "19-rendering"
css: "abcpdf-docs.css"
---

|  |  | PDF Rendering Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to render a PDF document. For an example of how to render a PDF direct to screen and how to print a PDF see the ABCpdfView project and classes under the ABCpdf menu item. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Read</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We create an ABCpdf Doc object and read our source PDF. [C#] ```csharp using Doc doc = new Doc(); doc.Read(Server.MapPath("../Rez/spaceshuttle.pdf")); ``` [Visual Basic] ```vbnet Dim doc As New Doc() doc.Read(Server.MapPath("../Rez/spaceshuttle.pdf")) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Prefs</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We specify our base rendering settings. [C#] ```csharp doc.Rendering.DotsPerInch = 36; ``` [Visual Basic] ```vbnet doc.Rendering.DotsPerInch = 36 ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Save</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Finally we save the first four pages of the document in png format. [C#] ```csharp for (int i = 1; i [Visual Basic] ```vbnet Dim i As Integer = 1 While i |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| shuttle_p1.png shuttle_p2.png shuttle_p3.png shuttle_p4.png |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>