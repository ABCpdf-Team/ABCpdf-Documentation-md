---
title: "filespecification"
css: "abcpdf-docs.css"
---

|  |  | FileSpecification Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| FileSpecification Constructor |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp FileSpecification(ObjectSoup soup) FileSpecification(ObjectSoup soup, string path) ``` [Visual Basic] ``` Sub New(soup As ObjectSoup) Sub New(soup As ObjectSoup, path As String) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created FileSpecification. | 
| path | A file to embed within the file specification. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create a FileSpecification. This constructor which takes a path to a file will embed and compress the file data using using the CompressFlate function. It will also insert appropriate metadata using the EmbeddedFileUpdateMetadata function. The constructor which takes an array of data will similarly embed and compress the data. However since there is no file path metadata will not be assigned. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The example below shows how to combine a set of PDF documents into a portfolio. See the Catalog.GetEmbeddedFiles function for how to extract files from a portfolio. [C#] ```csharp string[] files = { "SignedDocument.pdf", "spaceshuttle.pdf", "Authorization.pdf", "Portfolio1.pdf", }; using var doc = new Doc(); var fileSpecs = new List>(); foreach (string file in files) { byte[] data = null; using (var subDoc = new Doc()) { subDoc.Read(Server.MapPath(file)); data = subDoc.GetData(); } var embedFile = new EmbeddedFile(doc.ObjectSoup, data); embedFile.CompressFlate(); var fileSpec = new FileSpecification(doc.ObjectSoup); fileSpec.EmbeddedFile = embedFile; fileSpec.Uri = file; string name = Path.GetFileName(file); fileSpecs.Add(new Tuple(name, fileSpec)); } fileSpecs.Sort((a, b) => a.Item1.CompareTo(b.Item1)); // we do not really need to delete existing files but we do so as an example doc.SetInfo(doc.Root, "/Names*/EmbeddedFiles*/Names:Del", ""); foreach (var fileSpec in fileSpecs) { doc.SetInfo(doc.Root, "/Names*/EmbeddedFiles*/Names*[]:Text", fileSpec.Item1); doc.SetInfo(doc.Root, "/Names*/EmbeddedFiles*/Names*[]:Ref", fileSpec.Item2.ID); } // add placeholder text doc.AddText("This is a Adobe Acrobat Portfolio file. Please use Adobe Acrobat software to open it."); // save doc.ObjectSoup.Catalog.Version = 17; doc.SaveOptions.Linearize = false; doc.SetInfo(doc.Root, "/Collection*/D:Text", files[0]); doc.Save(Server.MapPath("createportfolio.pdf")); ``` [Visual Basic] ```vbnet Dim files As String() = {"SignedDocument.pdf", "spaceshuttle.pdf", "Authorization.pdf", "Portfolio1.pdf"} Using doc As New Doc() Dim fileSpecs = New List(Of Tuple(Of String, FileSpecification))() For Each file As String In files Dim data As Byte() = Nothing Using subDoc = New Doc() subDoc.Read(Server.MapPath(file)) data = subDoc.GetData() End Using Dim embedFile = New EmbeddedFile(doc.ObjectSoup, data) embedFile.CompressFlate() Dim fileSpec = New FileSpecification(doc.ObjectSoup) fileSpec.EmbeddedFile = embedFile fileSpec.Uri = file Dim name As String = Path.GetFileName(file) fileSpecs.Add(New Tuple(Of String, FileSpecification)(name, fileSpec)) Next fileSpecs.Sort(Function(a, b) a.Item1.CompareTo(b.Item1)) ' we do not really need to delete existing files but we do so as an example doc.SetInfo(doc.Root, "/Names*/EmbeddedFiles*/Names:Del", "") For Each fileSpec As var In fileSpecs doc.SetInfo(doc.Root, "/Names*/EmbeddedFiles*/Names*[]:Text", fileSpec.Item1) doc.SetInfo(doc.Root, "/Names*/EmbeddedFiles*/Names*[]:Ref", fileSpec.Item2.ID) Next ' add placeholder text doc.AddText("This is a Adobe Acrobat Portfolio file. Please use Adobe Acrobat software to open it.") ' save doc.ObjectSoup.Catalog.Version = 17 doc.SaveOptions.Linearize = False doc.SetInfo(doc.Root, "/Collection*/D:Text", files(0)) doc.Save(Server.MapPath("createportfolio.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>