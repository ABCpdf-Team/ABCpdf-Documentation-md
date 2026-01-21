---
title: "15-eform1"
css: "abcpdf-docs.css"
---

|  |  | eForm Fields Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to change the values of eForm fields. In this example we simply replace each of the fields in a form with the name of that field. |  |  | 

</td></tr> <tr> <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
 
Src</td><td width="14">&nbsp;</td><td valign="top"> 
| First we create an ABCpdf Doc object and read in our template form. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/form.pdf")); doc.Form.NeedAppearances = false; // for PDF 2.0 ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/form.pdf")) doc.Form.NeedAppearances = False ' for PDF 2.0 ``` |  |  | 
| --- | --- | --- |

</td></tr> <tr> <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
 
Add</td><td width="14">&nbsp;</td><td valign="top"> 
| We iterate through each of the top level fields. For each field we set the value of the field to be equal to the value of the name.[C#] ```csharp string[] names = doc.Form.GetFieldNames(); foreach (string theName in names) { var field = doc.Form[theName]; field.Value = field.Name; } ``` [Visual Basic] ```vbnet Dim theNames As String() = doc.Form.GetFieldNames() For Each theName As String In theNames Dim theField As Field = doc.Form(theName) theField.Value = theField.Name Next ``` |  |  | 
| --- | --- | --- |

</td></tr> 
<tr> <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
 
Save</td><td width="14">&nbsp;</td><td valign="top"> 
| Finally we save. [C#] ```csharp doc.Save(Server.MapPath("eformfields.pdf")); ``` [Visual Basic] ```vbnet doc.Save(Server.MapPath("eformfields.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td></tr> <tr> <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
 
Results</td><td width="14">&nbsp;</td><td valign="top"> 
| Given the following document. form.pdfThis is the kind of output you might expect. eformfields.pdf |  |  | 
| --- | --- | --- |

</td></tr> 
</table>