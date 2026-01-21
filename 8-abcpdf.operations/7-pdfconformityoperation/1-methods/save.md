---
title: "save"
css: "abcpdf-docs.css"
---

|  |  | Save Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Write the conforming PDF document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Save(Doc doc, string path) void Save(Doc doc, Stream stream) ``` [Visual Basic] ``` Sub Save(doc As Doc, path As String) Sub Save(doc As Doc, stream As Stream) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | The document. | 
| path | The destination file path. | 
| stream | The destination stream. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method writes the document in a conforming PDF format according to the Conformance property. Any conformance error is reported in the Errors property after the method finishes. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we save a document in PDF/A-1b format. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("mypics/Acrobat.pdf")); string path = Server.MapPath("pdfa_save.pdf"); using (var theOperation = new PdfConformityOperation()) { theOperation.Conformance = PdfConformance.PdfA1b; theOperation.Save(doc, path); if (theOperation.Errors.Count > 0) { Console.WriteLine("Errors:"); for (int i = 0; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("mypics/Acrobat.pdf")) Dim thePath As String = Server.MapPath("pdfa_save.pdf") Using theOperation As New PdfConformityOperation() theOperation.Conformance = PdfConformance.PdfA1b theOperation.Save(doc, thePath) If theOperation.Errors.Count > 0 Then Console.WriteLine("Errors:") Dim i As Integer = 0 While i |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>