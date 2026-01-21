---
title: "12-unicode"
css: "abcpdf-docs.css"
---

|  |  | Unicode Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to add complex scripts such as Chinese, Japanese and Korean. Here we choose to embed and subset our font to ensure our document renders correctly on all platforms. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Setup</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| First we create an ABCpdf Doc object and set the font size. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 32; ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 32 ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Read</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We read in our Japanese text from a Unicode text file. [C#] ```csharp string path = Server.MapPath("../Rez/Japanese2.txt"); string text = File.ReadAllText(path); ``` [Visual Basic] ```vbnet Dim thePath As String = Server.MapPath("../Rez/Japanese2.txt") Dim theText As String = File.ReadAllText(thePath) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Add</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Because we want to ensure that our document renders correctly on all platforms we're going to embed our font in Unicode format. We specify a left-to-right writing direction and we choose to subset our font. Please note when embedding fonts you must ensure you have permission to embed and redistribute the embedded font as part of your PDF. [C#] ```csharp doc.Page = doc.AddPage(); doc.Font = doc.EmbedFont("MS PGothic", LanguageType.Unicode, false, true); doc.AddText("Japanese" + text); ``` [Visual Basic] ```vbnet doc.Page = doc.AddPage() doc.Font = doc.EmbedFont("MS PGothic", LanguageType.Unicode, False, True) doc.AddText("Japanese" + theText) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Add</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Just to show how it works we'll also render a page in vertical writing mode. [C#] ```csharp doc.Page = doc.AddPage(); doc.Font = doc.EmbedFont("MS PGothic", LanguageType.Unicode, true, true); doc.AddText("Japanese" + text); ``` [Visual Basic] ```vbnet doc.Page = doc.AddPage() doc.Font = doc.EmbedFont("MS PGothic", LanguageType.Unicode, True, True) doc.AddText("Japanese" + theText) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Save</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Finally we save at a specified location. [C#] ```csharp doc.Save(Server.MapPath("unicode.pdf")); // finished ``` [Visual Basic] ```vbnet doc.Save(Server.MapPath("unicode.pdf")) End Using ' finished ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We get the following output. unicode.pdf - [Page 1] | unicode.pdf - [Page 2] | 
| --- | --- |

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
</table>