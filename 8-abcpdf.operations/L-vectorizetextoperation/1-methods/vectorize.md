---
title: "vectorize"
css: "abcpdf-docs.css"
---

# Vectorize Method

Vectorizes the text glyphs in the pages of a document.

## Syntax

**[C#]**

```csharp
void Vectorize(Doc doc)
void Vectorize(Pages pages)
void Vectorize(Page page)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub Vectorize(doc As Doc)
Sub Vectorize(pages As Pages)
Sub Vectorize(page As Page)
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| doc | The document containing the pages of text to be vectorized. | 
| pages | The pages of text to be vectorized as referenced by a Pages IndirectObject. | 
| page | The page of text to be vectorized as referenced by a Page IndirectObject. | 

## Notes

Vectorizes the text glyphs on pages in the document.

The VectorizeTextOperation operation removes font glyphs and replaces them with polygonal outlines that appear the same.

Note that pages may sometimes share content with other pages. If this is the case then vectorizing the text on one page will also vectorize it on other pages which use this shared content.

The [Operation.ProcessingObject](../../1-operation/3-events/1-processingobject.md) property is used to give the user some control over which fonts would be vectorized. Setting the ProcessingObjectEventArgs.Cancel to 'true' turns off the vectorization for the particular font that's passed in to the Processing method (see examples below)

Please see the [FontObject](../../../6-abcpdf.objects/fontobject/default.md) class for more information on the ProcessingObjectEventArgs.Object argument

The [Operation.ProcessedObject](../../1-operation/3-events/2-processedobject.md) property is not used with this operation

## Example

Here we vectorize all the text in the document.

[C#]

```csharp
static void VectorizeDocText1(string inDocName) {
  var op = new VectorizeTextOperation();
  using var doc = new Doc();
  doc.Read(Server.MapPath(inDocName));
  op.Vectorize(doc);
  doc.Save(Server.MapPath("VectorizedSample.pdf"));
}
```

[Visual Basic]

```vbnet
Private Shared Sub VectorizeDocText1(inDocName As String)
  Dim vecOp As New VectorizeTextOperation()
  Dim doc As New Doc()
  doc.Read(Server.MapPath(inDocName))
  vecOp.Vectorize(doc)
  doc.Save(Server.MapPath("VectorizedSample.pdf"))
End Sub
```

Here we Vectorize all but the bold text.

[C#]

```csharp
static void Vectorizing2(object sender, ProcessingObjectEventArgs e) {
  var font = e.Object as FontObject;
  if (font != null && font.BaseFont.Contains("Bold"))
    e.Cancel = true;
}
static void VectorizeDocText2(string inDocName) {
  var op = new VectorizeTextOperation();
  Doc doc = new Doc();
  doc.Read(Server.MapPath(inDocName));
  // Use the 'Vectorizing' method to decide which fonts to vectorize
  op.ProcessingObject += new ProcessingObjectEventHandler(Vectorizing2);
  op.Vectorize(doc);
  doc.Save(Server.MapPath("VectorizedSample.pdf"));
}
```

[Visual Basic]

```vbnet
Private Shared Sub Vectorizing2(sender As Object, e As ProcessingObjectEventArgs)
  Dim theFont As FontObject = TryCast(e.[Object], FontObject)
  If theFont <> Nothing AndAlso theFont.BaseFont.Contains("Bold") Then
    e.Cancel = True
  End If
End Sub
Private Shared Sub VectorizeDocText2(inDocName As String)
  Dim vecOp As New VectorizeTextOperation()
  Dim doc As New Doc()
  doc.Read(Server.MapPath(inDocName))
  ' Use the 'Vectorizing' method to decide which fonts to vectorize
  vecOp.ProcessingObject += New ProcessingObjectEventHandler(Vectorizing2)
  vecOp.Vectorize(doc)
  doc.Save(Server.MapPath("VectorizedSample.pdf"))
End Sub
```

Vectorize all the external fonts.

[C#]

```csharp
static void Vectorizing3(object sender, ProcessingObjectEventArgs e) {
  var font = e.Object as FontObject;
  if (font != null && font.EmbeddedFont != null)
    e.Cancel = true;
}
static void VectorizeDocText3(string inDocName) {
  var op = new VectorizeTextOperation();
  Doc doc = new Doc();
  doc.Read(Server.MapPath(inDocName));
  // Use the 'Vectorizing' method to decide which fonts to vectorize
  op.ProcessingObject += new ProcessingObjectEventHandler(Vectorizing3);
  op.Vectorize(doc);
  doc.Save(Server.MapPath("VectorizedSample.pdf"));
}
```

[Visual Basic]

```vbnet
Private Shared Sub Vectorizing3(sender As Object, e As ProcessingObjectEventArgs)
  Dim theFont As FontObject = TryCast(e.[Object], FontObject)
  If theFont <> Nothing AndAlso theFont.EmbeddedFont <> Nothing Then
    e.Cancel = True
  End If
End Sub
Private Shared Sub VectorizeDocText3(inDocName As String)
  Dim vecOp As New VectorizeTextOperation()
  Dim doc As New Doc()
  doc.Read(Server.MapPath(inDocName))
  ' Use the 'Vectorizing' method to decide which fonts to vectorize
  vecOp.ProcessingObject += New ProcessingObjectEventHandler(Vectorizing3)
  vecOp.Vectorize(doc)
  doc.Save(Server.MapPath("VectorizedSample.pdf"))
End Sub
```