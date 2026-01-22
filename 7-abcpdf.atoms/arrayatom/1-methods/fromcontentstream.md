# FromContentStream Function

Create an array of Atoms from a byte array containing a sequence of PDF objects

## Syntax

[C#]

```csharp
static <a href="../default.htm">ArrayAtom</a> FromContentStream(string text)static <a href="../default.htm">ArrayAtom</a> FromContentStream(byte[] data)static ArrayAtom FromContentStream(byte[] value, out IList&lt;int&gt; offsets)
```

[Visual Basic]

```vb
Shared Function FromContentStream(text As String) As <a href="../default.htm">ArrayAtom</a>Shared Function FromContentStream(data() As Byte) As <a href="../default.htm">ArrayAtom</a>Shared Function FromContentStream(data() As Byte, Out IList&lt;int&gt; offsets) As <a href="../default.htm">ArrayAtom</a>
```

## Params

| **Name** | **Description** |
| --- | --- |
| text | A string holding a sequence of atoms. |
| data | A chunk of data holding the sequence of atoms. |
| offsets | The byte offsets in the data for the start each of atom in the returned array. |
| return | An ArrayAtom holding the atoms in the content stream. |

## Notes

Create an array of Atoms from a byte array containing a sequence of PDF objects.

This method is useful for deconstructing PDF content streams for analysis and modification. To convert back into a content stream you can use the [Atom.GetData](1-atom/1-methods/getdata.md) function.

The returned offsets relate to the byte offsets for the start of each atom in the array that is returned.

## Example

This example shows how to use the FromContentStream function to parse and display a PDF content stream.

[C#]

```csharp
var sb = new StringBuilder();
using (var doc = new Doc()) {
  doc.Read(Server.MapPath("spaceshuttle.pdf"));
  var page = doc.ObjectSoup[doc.Page] as Page;
  var array = ArrayAtom.FromContentStream(page.GetContentData());
  int indent = 0;
  var indentPlus = new HashSet<string>(new string[] { "q", "BT" });
  var indentMinus = new HashSet<string>(new string[] { "Q", "ET" });
  var items = OpAtom.Find(array);
  int index = 0;
  foreach (var pair in items) {
    string op = ((OpAtom)array[pair.Item2]).Text;
    // add indent to code
    if (indentMinus.Contains(op))
      indent--;
    for (int i = 0; i < indent; i++)
      sb.Append(" ");
    // write out the operators
    for (int i = index; i <= pair.Item2; i++) {
      if (i != index)
        sb.Append(" ");
      var item = array[i];
      // we write arrays out individually so that
      // we can override default cr lf behavior
      var itemArray = item as ArrayAtom;
      if (itemArray != null) {
        int n = itemArray.Count;
        sb.Append("[");
        for (int j = 0; j < n; j++) {
          sb.Append(itemArray[j].ToString());
          if (j != n - 1)
            sb.Append(" ");
        }
        sb.Append("]");
      }
      else {
        sb.Append(item.ToString());
      }
    }
    sb.AppendLine();
    if (indentPlus.Contains(op))
      indent++;
    index = pair.Item2 + 1;
  }
  // write out any atoms that are left over
  for (int i = index; i < array.Count; i++) {
    sb.Append(" ");
    sb.Append(array[i].ToString());
  }
}
using (var doc = new Doc()) {
  doc.Font = doc.AddFont("Courier");
  doc.Rect.Inset(20, 20);
  doc.AddText(sb.ToString());
  doc.Save(Server.MapPath("PageContents.pdf"));
}
```

[Visual Basic]

```vb
Dim sb As New StringBuilder()
Using doc As New Doc()
  doc.Read(Server.MapPath("spaceshuttle.pdf"))
  Dim page As Page = TryCast(doc.ObjectSoup(doc.Page), Page)
  Dim array As ArrayAtom = ArrayAtom.FromContentStream(page.GetContentData())
  Dim indent As Integer = 0
  Dim indentPlus As New HashSet(Of String)(New String() {"q", "BT"})
  Dim indentMinus As New HashSet(Of String)(New String() {"Q", "ET"})
  Dim items As IList(Of Tuple(Of String, Integer)) = OpAtom.Find(array)
  Dim index As Integer = 0
  For Each pair As var In items
    Dim op As String = DirectCast(array(pair.Item2), OpAtom).Text
    ' add indent to code
    If indentMinus.Contains(op) Then
      System.Math.Max(System.Threading.Interlocked.Decrement(indent),indent + 1)
    End If
    Dim i As Integer = 0
    While i < indent
      sb.Append(" ")
      System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1)
    End While
    ' write out the operators
    Dim i As Integer = index
    While i <= pair.Item2
      If i <> index Then
        sb.Append(" ")
      End If
      Dim item As Atom = array(i)
      ' we write arrays out individually so that
      ' we can override default cr lf behavior
      Dim itemArray As ArrayAtom = TryCast(item, ArrayAtom)
      If itemArray <> Nothing Then
        Dim n As Integer = itemArray.Count
        sb.Append("[")
        Dim j As Integer = 0
        While j < n
          sb.Append(itemArray(j).ToString())
          If j <> n - 1 Then
            sb.Append(" ")
          End If
          System.Math.Max(System.Threading.Interlocked.Increment(j),j - 1)
        End While
        sb.Append("]")
      Else
        sb.Append(item.ToString())
      End If
      System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1)
    End While
    sb.AppendLine()
    If indentPlus.Contains(op) Then
      System.Math.Max(System.Threading.Interlocked.Increment(indent),indent - 1)
    End If
    index = pair.Item2 + 1
  Next
  ' write out any atoms that are left over
  Dim i As Integer = index
  While i < array.Count
    sb.Append(" ")
    sb.Append(array(i).ToString())
    System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1)
  End While
End Using
Using doc As New Doc()
  doc.Font = doc.AddFont("Courier")
  doc.Rect.Inset(20, 20)
  doc.AddText(sb.ToString())
  doc.Save(Server.MapPath("PageContents.pdf"))
End Using
```

![](../../../images/pdf/pagecontents.pdf.png)
PageContents.pdf

