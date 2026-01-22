# Vectorize Method

Vectorizes the text glyphs in the pages of a document.

## Syntax

[C#]

```csharp
void Vectorize(Doc doc)void Vectorize(Pages pages)void Vectorize(Page page)
```

[Visual Basic]

```vb
Sub Vectorize(doc As Doc)Sub Vectorize(pages As Pages)Sub Vectorize(page As Page)
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | The document containing the pages of text to be vectorized. |
| pages | The pages of text to be vectorized as referenced by a Pages IndirectObject. |
| page | The page of text to be vectorized as referenced by a Page IndirectObject. |

## Notes

Vectorizes the text glyphs on pages in the document.

The VectorizeTextOperation operation removes font glyphs and replaces them with polygonal outlines that appear the same.

Note that pages may sometimes share content with other pages. If this is the case then vectorizing the text on one page will also vectorize it on other pages which use this shared content.

The [Operation.ProcessingObject](1-operation/3-events/1-processingobject.md) property is used to give the user some control over which fonts would be vectorized. Setting the ProcessingObjectEventArgs.Cancel to 'true' turns off the vectorization for the particular font that's passed in to the Processing method (see examples below)

Please see the [FontObject](6-abcpdf.objects/fontobject/default.md) class for more information on the ProcessingObjectEventArgs.Object argument

The [Operation.ProcessedObject](1-operation/3-events/2-processedobject.md) property is not used with this operation

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

```vb
Private Shared Sub VectorizeDocText1(inDocName As String)
  Dim vecOp As New VectorizeTextOperation()
  Dim doc As New Doc()
  doc.Read(Server.MapPath(inDocName))
  vecOp.Vectorize(doc)
  doc.Save(Server.MapPath("VectorizedSample.pdf"))
End Sub
```

