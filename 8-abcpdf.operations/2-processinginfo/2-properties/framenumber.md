# FrameNumber Property

| **Type** | **Default** | **Read Only** | **Description** |
| --- | --- | --- | --- |
| [C#] <BR> `long?` | n/a | No | Gets or sets the frame number of the source frame being/to be processed. |

## Notes

The value of this property when the [Operation.ProcessingObject](1-operation/3-events/1-processingobject.md) event is generated depends on the operation.

The event handler should change this value when a processing sequence other than the default is desired. Set this value to null to end the processing of the current set of frames.

## Example

[C#]

```csharp
using var doc = new Doc();
using (var operation = new SwfImportOperation()) {
  operation.Doc = doc;
  operation.ContentAlign = ContentAlign.Top;
  operation.ContentScaleMode = ContentScaleMode.ShowAll;
  operation.ProcessingObject += delegate (object sender, ProcessingObjectEventArgs e) {
    if (e.Info.SourceType == ProcessingSourceType.MultiFrameImage && e.Info.FrameNumber.HasValue)
      e.Info.FrameNumber = 1 + (long)(e.Info.FrameRate.Value * 3.5);
  };
  operation.Import(Server.MapPath("ABCpdf.swf"));
}
doc.Save(Server.MapPath("swf.pdf"));
```

[Visual Basic]

```vb
Using doc As New Doc()
  Using operation As New SwfImportOperation()
    operation.Doc = doc
    operation.ContentAlign = ContentAlign.Top
    operation.ContentScaleMode = ContentScaleMode.ShowAll
    operation.ProcessingObject += Sub(sender As Object, e As ProcessingObjectEventArgs) If e.Info.SourceType = ProcessingSourceType.MultiFrameImage AndAlso e.Info.FrameNumber.HasValue Then
      e.Info.FrameNumber = 1 + DirectCast(e.Info.FrameRate.Value * 3.5, Long)
    End If
    operation.Import(Server.MapPath("ABCpdf.swf"))
  End Using
  doc.Save(Server.MapPath("swf.pdf"))
End Using
```

Also see example code in: [SwfImportOperation Import Function](5-swfimportoperation/1-methods/import.md).
