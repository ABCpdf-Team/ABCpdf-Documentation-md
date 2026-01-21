---
title: "writepageseparator"
css: "abcpdf-docs.css"
---

# WritePageSeparator Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp XSaveOptions.PageSeparatorMethod ``` [Visual Basic]`XSaveOptions.PageSeparatorMethod` | null | No | The delegate called to write the page separator for export. | 

## Notes

This delegate is called during HTML export.

If it is null, a default page separator is produced for each page. You can customize the page separator by setting this property.

The definition of the XSaveOptions.PageSeparatorMethod delegate is as follows.

[C#]

```csharp
delegate void PageSeparatorMethod(int pageNum, ExportArgs e);
```

<span class=language>[Visual&nbsp;Basic]</span>
```vbnet
Delegate Sub PageSeparatorMethod(pageNum As Integer, e As ExportArgs)
```

pageNum is the page number, starting with 1.

The page separator is to be written to e.Writer. e.Writer is an XmlWriter for HTML export.

## Example

The following example shows how to customize the page separator.

[C#]

```csharp
using var doc = new Doc();
doc.Read(Server.MapPath("../mypics/sample.pdf"));
doc.SaveOptions.WritePageSeparator = delegate (int pageNum, XSaveOptions.ExportArgs e) {
  var writer = (XmlWriter)e.Writer;
  if (pageNum > 1) {
    writer.WriteStartElement("hr");
    writer.WriteEndElement();
  }
  writer.WriteStartElement("div");
  writer.WriteAttributeString("align", "right");
  writer.WriteString(string.Format("Page {0}", pageNum));
  writer.WriteFullEndElement();
};
doc.Save(Server.MapPath("PageSeparator.htm"));
doc.Dispose();
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc()
  doc.Read(Server.MapPath("../mypics/sample.pdf"))
  doc.SaveOptions.WritePageSeparator = Sub(pageNum As Integer, e As XSaveOptions.ExportArgs)
  Dim writer As XmlWriter = DirectCast(e.Writer, XmlWriter)
  If pageNum > 1 Then
    writer.WriteStartElement("hr")
    writer.WriteEndElement()
  End If
  writer.WriteStartElement("div")
  writer.WriteAttributeString("align", "right")
  writer.WriteString(String.Format("Page {0}", pageNum))
  writer.WriteFullEndElement()

  End Sub
  doc.Save(Server.MapPath("PageSeparator.htm"))
  doc.Dispose()
End Using
```