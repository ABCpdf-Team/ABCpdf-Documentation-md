---
title: "read"
css: "abcpdf-docs.css"
---

|  |  | Read Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Read and validate an existing document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Doc Read(string path, XReadOptions options) Doc Read(byte[] data, XReadOptions options) Doc Read(Stream stream, XReadOptions options) ``` [Visual Basic] ``` Function Read(path As String, options As XReadOptions) As Doc Function Read(data() As Byte, options As XReadOptions) As Doc Function Read(stream As Stream, options As XReadOptions) As Doc ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The file path to PDF document. | 
| data | The source PDF data. | 
| stream | The source PDF stream. | 
| options | The settings for the read. (May be null.) | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method reads and validates the document according to the Conformance property. Any conformance error or warning is reported in the Errors property or the Warnings property after the method finishes. If the Doc property is null, the document is read into a new Doc object, which is returned; otherwise, the document is read into the value of the Doc property, which is returned. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we validate a document against PDF/A-1b format. [C#] ```csharp string path = Server.MapPath("pdfa.pdf"); using (var op = new PdfValidationOperation()) { op.Conformance = PdfConformance.PdfA1b; using var doc = op.Read(path, null); if (op.Errors.Count > 0) { Console.WriteLine("Errors:"); for (int i = 0; i 0) { if (op.Errors.Count > 0) Console.WriteLine(); Console.WriteLine("Warnings:"); for (int i = 0; i [Visual Basic] ```vbnet Dim thePath As String = Server.MapPath("pdfa.pdf") Using theOperation As New PdfValidationOperation() theOperation.Conformance = PdfConformance.PdfA1b Dim doc As Doc = theOperation.Read(thePath, Nothing) doc.Dispose() If theOperation.Errors.Count > 0 Then Console.WriteLine("Errors:") Dim i As Integer = 0 While i 0 Then If theOperation.Errors.Count > 0 Then Console.WriteLine() End If Console.WriteLine("Warnings:") Dim i As Integer = 0 While i |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>