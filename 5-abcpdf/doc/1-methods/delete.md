---
title: "delete"
css: "abcpdf-docs.css"
---

|  |  | Delete Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Deletes an object previously added to the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Delete(int id) ``` [Visual Basic] ``` Sub Delete(id As Integer) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the object to be deleted. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to delete an object previously added to the document. Deletion may be applied to pages to remove them from the document. For example to delete the current page you might use the following code: [C#] ```csharp theDoc.Delete(theDoc.Page); ``` [Visual Basic] ```vbnet theDoc.Delete(theDoc.Page) ``` However if you are deleting multiple pages you will probably find it more efficient to use the RemapPages method. as this is more optimized for moving and removing pages. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code snippet illustrates how one might add an image and then delete it if the image color space is CMYK. [C#] ```csharp using var doc = new Doc(); string path = Server.MapPath("../mypics/mypic.jpg"); int id1 = doc.AddImageFile(path, 1); int id2 = doc.GetInfoInt(id1, "XObject"); int comps = doc.GetInfoInt(id2, "Components"); if (comps == 4) doc.Delete(id1); doc.Save(Server.MapPath("docdelete.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") Dim theID1 As Integer = doc.AddImageFile(thePath, 1) Dim theID2 As Integer = doc.GetInfoInt(theID1, "XObject") Dim theComps As Integer = doc.GetInfoInt(theID2, "Components") If theComps = 4 Then doc.Delete(theID1) End If doc.Save(Server.MapPath("docdelete.pdf")) End Using ``` docdelete.pdf Also see example code in: ABCpdf Deletion Example, ABCpdf eForm Placeholder Example. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>