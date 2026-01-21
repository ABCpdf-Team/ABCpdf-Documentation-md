---
title: "05-deletion"
css: "abcpdf-docs.css"
---

|  |  | Deletion Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to delete pages from a PDF document. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Setup</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| First we create an ABCpdf Doc object and read our source document. We store the number of pages we're going to delete - we're going to delete all but one. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); int count = doc.PageCount - 1; ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) Dim theCount As Integer = doc.PageCount - 1 ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Delete</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We go round a loop deleting the second page each time. [C#] ```csharp for (int i = 0; i [Visual Basic] ```vbnet Dim i As Integer = 0 While i |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Save</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We add some text to the PDF so that we know how many pages we've deleted. Finally we save the PDF. [C#] ```csharp doc.FontSize = 500; doc.Color.String = "255 0 0"; doc.TextStyle.HPos = 0.5; doc.TextStyle.VPos = 0.3; doc.AddText(count.ToString()); doc.Save(Server.MapPath("deletion.pdf")); ``` [Visual Basic] ```vbnet doc.FontSize = 500 doc.Color.String = "255 0 0" doc.TextStyle.HPos = 0.5 doc.TextStyle.VPos = 0.3 doc.AddText(theCount.ToString()) doc.Save(Server.MapPath("deletion.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| deletion.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>