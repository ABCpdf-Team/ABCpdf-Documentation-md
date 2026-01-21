# GetEmbeddedFiles Function

Gets all the embedded files in this document

## Syntax

**[C#]**

```csharp
IDictionaryFileSpecification> GetEmbeddedFiles()
```

<span class=language>[Visual
            Basic]</span>  

            `Function GetEmbeddedFiles() As IDictionaryFileSpecification>`
## Params

| Name | Description | 
| --- | --- |
| return | A set of names and the file associated with each name. | 

## Notes

Gets all the embedded files in this document.

PDF documents can contain a set of named files. These files can then be referenced by name elsewhere in the document.

The most common case in which named files are used is in the case of PDF portfolios. Adobe now uses the name Portfolio for this type of document but in the PDF specification they are known as Portable Collections. While the names may vary, the two are the same.

PDF Portfolios appear as one PDF document but actually contain many. Typically the first document represents the visible face of the collection when opened. After the collection is open you can switch between the embedded PDFs.

PDF portfolios can be used to represent a folder of PDFs. For example you might find a portable collection being used to display multiple emails within a single PDF Portfolio.

## Example

The example below show how to extract all the files embedded in a PDF portfolio. See the [FileSpecification constructor](../../../6-abcpdf.objects/filespecification/1-methods/filespecification.md) for the creation of portfolios.

[C#]

```csharp
using var doc = new Doc();
var ro = new XReadOptions();
ro.OpenPortfolios = false;
doc.Read(Server.MapPath("Portfolio1.pdf"), ro);
var files = doc.ObjectSoup.Catalog.GetEmbeddedFiles();
foreach (var pair in files) {
  var fileSpec = pair.Value;
  fileSpec.Rationalize();
  var file = fileSpec.EmbeddedFile;
  if ((file != null) && (file.Decompress())) {
    string name = "Portfolio_" + fileSpec.Uri;
    string path = name;
    File.WriteAllBytes(path, file.GetData());
  }
}
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc()
  Dim ro As New XReadOptions()
  ro.OpenPortfolios = False
  doc.Read(Server.MapPath("Portfolio1.pdf"), ro)
  Dim files = doc.ObjectSoup.Catalog.GetEmbeddedFiles()
  For Each pair As var In files
    Dim fileSpec As FileSpecification = pair.Value
    fileSpec.Rationalize()
    Dim file__1 As EmbeddedFile = fileSpec.EmbeddedFile
    If (file__1 <> Nothing) AndAlso (file__1.Decompress()) Then
      Dim name As String = "Portfolio_" + fileSpec.Uri
      Dim path As String = name
      File.WriteAllBytes(path, file__1.GetData())
    End If
  Next
End Using
```