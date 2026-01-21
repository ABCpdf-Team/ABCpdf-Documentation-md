---
title: "setinfo"
css: "abcpdf-docs.css"
---

|  |  | SetInfo Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets information about an object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetInfo(int id, string type, string info) void SetInfo(int id, string type, int info) void SetInfo(int id, string type, double info) void SetInfo(int id, string type, DateTime info) void SetInfo(int id, string type, bool info) ``` [Visual Basic] ``` Sub SetInfo(id As Integer, type As String, info As String) Sub SetInfo(id As Integer, type As String, info As Integer) Sub SetInfo(id As Integer, type As String, info As Double) Sub SetInfo(id As Integer, type As String, info As DateTime) Sub SetInfo(id As Integer, type As String, info As Boolean) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the object to be modified. | 
| type | The type of value to insert. | 
| info | The value to insert.• The overloads taking integer/floating-point info converts this parameter to the string representation (numbers as used in PDF) in the invariant culture without creating a managed string object.• The overload taking DateTime info converts this parameter to the string representation (PDF date string) so it is mostly used with the :Text object type. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| In the same way as you can get information about aspects of a document using the GetInfo method you can modify aspects of the document using the SetInfo method. Different types of object support different types of properties. For more detailed information see the Object Paths section of this document. PDF objects are case sensitive so be sure you use the correct case. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following shows how to modify the document catalog to ensure that the PDF opens onto the second page rather than the first. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); int pages = doc.GetInfoInt(doc.Root, "Pages"); int page2 = doc.GetInfoInt(pages, "Page 2"); string action = $"[ {page2} 0 R /Fit ]"; doc.SetInfo(doc.Root, "/OpenAction", action); doc.Save(Server.MapPath("docsetinfo.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) Dim thePages As Integer = doc.GetInfoInt(doc.Root, "Pages") Dim thePage2 As Integer = doc.GetInfoInt(thePages, "Page 2") Dim theAction As String = $"[ {thePage2} 0 R /Fit ]" doc.SetInfo(doc.Root, "/OpenAction", theAction) doc.Save(Server.MapPath("docsetinfo.pdf")) End Using ``` Open Actions. The way in which a PDF is displayed when opened is dependent on certain flags within the PDF itself. Here are some common combinations. For full details of how these work you should see the Adobe PDF Specification available from the Adobe web site. To show outlines: ```generic theDoc.SetInfo(theDoc.Root, "/PageMode", "/UseOutlines") ``` Or for thumbnails: ```generic theDoc.SetInfo theDoc.Root, "/PageMode", "/UseThumbs" ``` To display two pages side by side: ```generic theDoc.SetInfo(theDoc.Root, "/PageLayout", "/TwoColumnLeft") ``` To make the print dialog appear when the document is opened: ```generic theDoc.SetInfo(theDoc.Root, "/OpenAction", ">") ``` To open at 200% zoom onto the current page: ```generic theDoc.SetInfo(theDoc.Root, "/OpenAction", "[ " + theDoc.Page.ToString() +" 0 R /XYZ null null 2 ]") ``` To fit the document width onto the current page: ```generic theDoc.SetInfo(theDoc.Root, "/OpenAction", "[ " + theDoc.Page.ToString() + " 0 R /FitH " + theDoc.MediaBox.Height.ToString() + " ]") ``` | 
| --- |

Also see example code in: [ABCpdf Landscape Example](../../../4-examples/08-landscape.md), [ABCpdf Fields, Markup and Movies Example](../../../4-examples/18-annotations.md), [Doc AddObject Function](addobject.md), [Doc ColorSpace Property](../2-properties/colorspace.md), [FileSpecification FileSpecification Function](../../../6-abcpdf.objects/filespecification/1-methods/filespecification.md), [OpAtom Find Function](../../../7-abcpdf.atoms/opatom/1-methods/find.md), [XpsImportOperation Import Function](../../../8-abcpdf.operations/4-xpsimportoperation/1-methods/import.md).

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>