---
title: "16-eformfdf"
css: "abcpdf-docs.css"
---

|  |  | eForm FDF Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to extract Unicode annotation values from an eForm FDF file. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Src</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| First we create an ABCpdf Doc object and read in our FDF file. [C#] ```csharp using var fdf = new Doc(); fdf.Read(Server.MapPath("../Rez/form.fdf")); ``` [Visual Basic] ```vbnet Dim theFDF As New Doc() theFDF.Read(Server.MapPath("../Rez/form.fdf")) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Dest</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We find out how many items there are in the FDF file and prepare to iterate through them. [C#] ```csharp string theValues = ""; int lastID = Convert.ToInt32(fdf.GetInfo(0, "Count")); ``` [Visual Basic] ```vbnet Dim theValues As String = "" Dim theLastID As Integer = Convert.ToInt32(theFDF.GetInfo(0, "Count")) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Add</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We go through each item. We check to see if it is an annotation. If it is we check to see if the annotation type is text. If we have found a text annotation we extract the content and add the value to our list. [C#] ```csharp // extract annotation values (for insertion into PDF) for (int i = 0; i [Visual Basic] ```vbnet ' extract annotation values (for insertion into PDF) Dim i As Integer = 0 While i |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Save</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Finally we add the Unicode text to a new document and save it. [C#] ```csharp using var doc = new Doc(); doc.Font = doc.EmbedFont("Arial", LanguageType.Unicode, false, true); doc.FontSize = 96; doc.Rect.Inset(10, 10); doc.AddText(theValues); doc.Save(Server.MapPath("fdf.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Font = doc.EmbedFont("Arial", LanguageType.Unicode, False, True) doc.FontSize = 96 doc.Rect.Inset(10, 10) doc.AddText(theValues) doc.Save(Server.MapPath("fdf.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This is the kind of PDF you might expect to produce. fdf.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>