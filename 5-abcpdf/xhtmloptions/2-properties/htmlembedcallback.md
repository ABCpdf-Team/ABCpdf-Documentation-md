# HtmlEmbedCallback Property

| **Type** | **Default** | **Read Only** | **Description** |
| --- | --- | --- | --- |
| [C#] <BR> `HtmlEmbedCallback` | null | No | The multicast delegate to be called when embedding an object while HTML rendering is taking place. |

## Notes

This delegate is called when embedding an object.

Objects embedded in HTML, such as those with the embed HTML tags, will trigger the callback if they are of certain content types. This callback provides a way to change the parameters of the embedded objects.

The definition of the HtmlEmbedCallback multicast delegate is as follows.

[C#]delegate void HtmlEmbedCallback([Doc](doc/default.md) doc, HtmlEmbedInfo info); [Visual Basic]Delegate Sub HtmlEmbedCallback(doc As [Doc](doc/default.md), info As HtmlEmbedInfo);

doc is the target Doc for the added HTML. The properties of HtmlEmbedInfo are as follows:

Parameters depends on EmbedType as follows:

The values in HtmlParameterDictionary are of type HtmlParameter.

## Example

The following example shows the effect that this parameter has on HTML rendering.

[C#]

```csharp
using var doc = new Doc();
string uri = "https://www.websupergoo.com/";
// Set up the callback
doc.HtmlOptions.HtmlEmbedCallback = (Doc d, HtmlEmbedInfo info) => {
  if (info.EmbedType == HtmlEmbedType.Swf) {
    HtmlParameter param;
    if (info.Parameters.TryGetValue("dataURL", out param)) {
      info.Parameters.Remove("dataURL");
      param.Conversion = HtmlParameterConversionType.UrlToTextFileContent;
      info.Parameters["dataXML"] = param;
    }
  }
};
// Render html page
doc.AddImageUrl(uri);
// Save the document
doc.Save(Server.MapPath("HtmlOptionsEmbedCallback.pdf"));
```

[Visual Basic]

```vb
Using doc As New Doc()
  Dim theURL As String = "https://www.websupergoo.com/"
  ' Set up the callback
  doc.HtmlOptions.HtmlEmbedCallback = Function(d As Doc, info As HtmlEmbedInfo) 
  If info.EmbedType = HtmlEmbedType.Swf Then
    Dim param As HtmlParameter
    If info.Parameters.TryGetValue("dataURL", param) Then
      info.Parameters.Remove("dataURL")
      param.Conversion = HtmlParameterConversionType.UrlToTextFileContent
      info.Parameters("dataXML") = param
    End If
  End If

  End Function
  ' Render html page
  doc.AddImageUrl(theURL)
  ' Save the document
  doc.Save(Server.MapPath("HtmlOptionsEmbedCallback.pdf"))
End Using
```

