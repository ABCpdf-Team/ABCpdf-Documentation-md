---
title: "15-eform3"
css: "abcpdf-docs.css"
---

|  |  | eForm Stamp Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to stamp eForm fields into a document so that the values are indelibly marked |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Src</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| First we create an ABCpdf Doc object and read in our template form. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/form.pdf")); doc.Form.NeedAppearances = false; // for PDF 2.0 doc.Font = doc.AddFont("Helvetica-Bold"); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/form.pdf")) doc.Form.NeedAppearances = False ' for PDF 2.0 doc.Font = doc.AddFont("Helvetica-Bold") ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Add</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We set the values of selected fields and then we stamp all field values into the document. [C#] ```csharp doc.Form["Day"].Value = "23"; doc.Form["Month"].Value = "February"; doc.Form["Year"].Value = "2005"; doc.Form["State"].Value = "Arizona"; doc.Form.Stamp(); ``` [Visual Basic] ```vbnet doc.Form("Day").Value = "23" doc.Form("Month").Value = "February" doc.Form("Year").Value = "2005" doc.Form("State").Value = "Arizona" doc.Form.Stamp() ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Save</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Finally we save. [C#] ```csharp doc.Save(Server.MapPath("eformstamp.pdf")); ``` [Visual Basic] ```vbnet doc.Save(Server.MapPath("eformstamp.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Given the following document. form.pdf This is the kind of output you might expect. eformstamp.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>