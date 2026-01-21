---
title: "save"
css: "abcpdf-docs.css"
---

# Save Function

Write the conforming PDF document.

## Syntax

**[C#]**

```csharp
void Save(Doc doc, string path)
void Save(Doc doc, Stream stream)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub Save(doc As Doc, path As String)
Sub Save(doc As Doc, stream As Stream)
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| doc | The document. | 
| path | The destination file path. | 
| stream | The destination stream. | 

## Notes

This method writes the document in a conforming PDF format according to the [Conformance](../2-properties/conformance.md) property. Any conformance error is reported in the [Errors](../2-properties/errors.md) property after the method finishes.

## Example

Here we save a document in PDF/A-1b format.

[C#]

```csharp
using var doc = new Doc();
doc.Read(Server.MapPath("mypics/Acrobat.pdf"));
string path = Server.MapPath("pdfa_save.pdf");
using (var theOperation = new PdfConformityOperation()) {
  theOperation.Conformance = PdfConformance.PdfA1b;
  theOperation.Save(doc, path);

  if (theOperation.Errors.Count > 0) {
    Console.WriteLine("Errors:");
    for (int i = 0; i < theOperation.Errors.Count; ++i)
      Console.WriteLine(theOperation.Errors[i]);
  }
}
```

<span class=language>[Visual
            Basic]</span>
```vbnet
Using doc As New Doc()
  doc.Read(Server.MapPath("mypics/Acrobat.pdf"))
  Dim thePath As String = Server.MapPath("pdfa_save.pdf")
  Using theOperation As New PdfConformityOperation()
    theOperation.Conformance = PdfConformance.PdfA1b
    theOperation.Save(doc, thePath)

    If theOperation.Errors.Count > 0 Then
      Console.WriteLine("Errors:")
      Dim i As Integer = 0
      While i < theOperation.Errors.Count
        Console.WriteLine(theOperation.Errors(i))
        System.Threading.Interlocked.Increment(i)
      End While
    End If
  End Using
End Using
```