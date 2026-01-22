# Group  Function

Group a range of text fragments into a set of lines.

## Syntax

[C#]

```csharp
IList&lt;<a href="../../8-textgroup/default.htm">TextGroup</a>&gt; Group(List&lt;<a href="../../8-textfragment/default.htm">TextFragment</a>&gt; fragments)
```

[Visual Basic]

```vb
Function Group(fragments As List&lt;<a href="../../8-textfragment/default.htm">TextFragment</a>&gt;) As IList&lt;<a href="../../8-textgroup/default.htm">TextGroup</a>&gt;
```

## Params

| **Name** | **Description** |
| --- | --- |
| fragments | The fragments to be grouped. |
| Return | Returns a list of groups defining the words. |

## Notes

Group a range of text fragments into a set of lines.

Calling Select will return a list of TextFragments corresponding to the section of text you are interested in. However each TextFragment may only make up a small portion of a word. Calling this function allows you to group connected fragments into continuous sections with a common rectangular area.

Strictly speaking this grouping does not always correspond to lines. For example two fragments on the same line, separated by a large distance, will not be considered contiguous. However for most purposes the two broadly correspond.

## Example

Here we highlight a set of words in a source document by drawing a rectangle around each one.

[C#]

```csharp
string src = Server.MapPath("mypics/Acrobat.pdf");
string dst = Server.MapPath("HighlightedText.pdf");
string searchString = "Acrobat";
using var doc = new Doc();
doc.Read(src);
TextOperation op = new TextOperation(doc);
op.PageContents.AddPages();
string text = op.GetText();
int pos = 0;
while (true) {
  pos = text.IndexOf(searchString, pos, StringComparison.CurrentCultureIgnoreCase);
  if (pos < 0)
    break;
  var selection = op.Select(pos, searchString.Length);
  var groups = op.Group(selection);
  foreach (var group in groups) {
    doc.Rect.String = group.Rect.String;
    doc.FrameRect();
  }
  pos += searchString.Length;
}
doc.Save(dst);
```

[Visual Basic]

```vb
Dim theSrc As String = Server.MapPath("mypics/Acrobat.pdf")
Dim theDst As String = Server.MapPath("HighlightedText.pdf")
Dim searchString As String = "Acrobat"
Using doc As New Doc()
  doc.Read(theSrc)
  Dim op As New TextOperation(doc)
  op.PageContents.AddPages()
  Dim text As String = op.GetText()
  Dim pos As Integer = 0
  While True
    pos = text.IndexOf(searchString, pos, StringComparison.CurrentCultureIgnoreCase)
    If pos < 0 Then
      Exit While
    End If
    Dim theSelection As IList(Of TextFragment) = op.[Select](pos, searchString.Length)
    Dim theGroups As IList(Of TextGroup) = op.Group(theSelection)
    For Each theGroup As TextGroup In theGroups
      doc.Rect.String = theGroup.Rect.[String]
      doc.FrameRect()
    Next
    pos += searchString.Length
  End While
  doc.Save(theDst)
End Using
```

