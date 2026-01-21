---
title: "read"
css: "abcpdf-docs.css"
---

# Read Function

Read and validate an existing document.

## Syntax

**[C#]**

```csharp
Doc Read(string path, XReadOptions options)
Doc Read(byte[] data, XReadOptions options)
Doc Read(Stream stream, XReadOptions options)
```

<span class=language>[Visual
            Basic]</span>  

```
Function Read(path As String, options As XReadOptions) As Doc
Function Read(data() As Byte, options As XReadOptions) As Doc
Function Read(stream As Stream, options As XReadOptions) As Doc
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| path | The file path to PDF document. | 
| data | The source PDF data. | 
| stream | The source PDF stream. | 
| options | The settings for the read. (May be null.) | 

## Notes

This method reads and validates the document according to the [Conformance](../2-properties/conformance.md) property. Any conformance error or warning is reported in the [Errors](../2-properties/errors.md) property or the [Warnings](../2-properties/warnings.md) property after the method finishes.

If the [Doc](../2-properties/doc.md) property is null, the document is read into a new [Doc](../../../5-abcpdf/doc/default.md) object, which is returned; otherwise, the document is read into the value of the [Doc](../2-properties/doc.md) property, which is returned.

## Example

Here we validate a document against PDF/A-1b format.

[C#]

```csharp
string path = Server.MapPath("pdfa.pdf");
using (var op = new PdfValidationOperation()) {
  op.Conformance = PdfConformance.PdfA1b;
  using var doc = op.Read(path, null);

  if (op.Errors.Count > 0) {
    Console.WriteLine("Errors:");
    for (int i = 0; i  0) {
    if (op.Errors.Count > 0)
      Console.WriteLine();
    Console.WriteLine("Warnings:");
    for (int i = 0; i < op.Warnings.Count; ++i)
      Console.WriteLine(op.Warnings[i]);
  }
}
```

<span class=language>[Visual
            Basic]</span>
```vbnet
Dim thePath As String = Server.MapPath("pdfa.pdf")
Using theOperation As New PdfValidationOperation()
  theOperation.Conformance = PdfConformance.PdfA1b
  Dim doc As Doc = theOperation.Read(thePath, Nothing)
  doc.Dispose()

  If theOperation.Errors.Count > 0 Then
    Console.WriteLine("Errors:")
    Dim i As Integer = 0
    While i  0 Then
    If theOperation.Errors.Count > 0 Then
      Console.WriteLine()
    End If
    Console.WriteLine("Warnings:")
    Dim i As Integer = 0
    While i < theOperation.Warnings.Count
      Console.WriteLine(theOperation.Warnings(i))
      System.Threading.Interlocked.Increment(i)
    End While
  End If
End Using
```