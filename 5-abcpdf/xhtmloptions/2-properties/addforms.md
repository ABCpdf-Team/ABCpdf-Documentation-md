---
title: "addforms"
css: "abcpdf-docs.css"
---

|  |  | AddForms Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether form fields should be live. | 

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
      
| This property determines whether form fields in HTML are reproduced as form fields in the final PDF output. Form fields in PDF do not work exactly the same as form fields in HTML so while the results will be similar they may not be identical. The ABCChrome engine relies on JavaScript for this feature, so if you set the UseScript property to false, it will cease to operate. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows the effect that this parameter has on HTML rendering. [C#] ```csharp using var doc = new Doc(); // Covert html form fields to the pdf form fields in the output file doc.HtmlOptions.AddForms = true; int id = doc.AddImageUrl("https://www.nasa.gov/forms/submit-a-question-for-nasa/"); // Save the document doc.Save(Server.MapPath("HtmlOptionsAddForms.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() ' Covert html form fields to the pdf form fields in the output file doc.HtmlOptions.AddForms = True Dim id As Integer = doc.AddImageUrl("https://www.websupergoo.com/thank-you-for-downloading.aspx") ' Save the document doc.Save(Server.MapPath("HtmlOptionsAddForms.pdf")) End Using ``` HtmlOptionsAddForms.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>