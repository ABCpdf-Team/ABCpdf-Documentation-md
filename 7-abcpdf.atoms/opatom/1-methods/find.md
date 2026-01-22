# Find Function

Finds specified types of OpAtom entries in an array

## Syntax

[C#]

```csharp
IList&lt;Tuple&lt;string, int&gt;&gt; Find(<a href="../../arrayatom/default.htm">ArrayAtom</a> atom)IList&lt;Tuple&lt;string, int&gt;&gt; Find(<a href="../../arrayatom/default.htm">ArrayAtom</a> atom, string[] names)
```

[Visual Basic]

```vb
Function Find(atom As <a href="../../arrayatom/default.htm">ArrayAtom</a>) As IList(Of Tuple(Of string, int))Function Find(atom As <a href="../../arrayatom/default.htm">ArrayAtom</a>, names() As String) As IList(Of Tuple(Of string, int))
```

## Params

| **Name** | **Description** |
| --- | --- |
| atom | The ArrayAtom to be searched. |
| names | The types of OpAtoms that should be returned. |
| return | The positions and text of the items which were found. |

## Notes

Finds specified types of OpAtom entries in an array.

If you specify no names then the positions and text of all the OpAtoms in the ArrayAtom will be returned. If you are only interested in a particular set of operators then you can specify an array of those types to restrict the number of items returned.

In addition to the standard names there is also the "Meta:InlineImage" name which is a metatag to allow you to access inline image streams. By explicitly setting this - it must be explicitly provided - you can pick up the location of any inline image dictionaries.

## Example

This example shows how to use the [Array.FromContentStream](arrayatom/1-methods/fromcontentstream.md) function to parse a content stream and then use the Find method to search for certain types of color operators and replace them with other color operators. In this example this has the effect of converting some black parts of the PDF to red. For a more comprehensive approach one would use the [ContentStreamOperation](8-abcpdf.operations/G-contentstreamoperation/default.md) class to determine all content streams associated with the pages in question.

[C#]

```csharp
using var doc = new Doc();
doc.Read(Server.MapPath("spaceshuttle.pdf"));
doc.RemapPages(new int[] { 1, 1 });
doc.PageNumber = 2;
var page = doc.ObjectSoup[doc.Page] as Page;
var layers = page.GetLayers();
using var st = new MemoryStream();
foreach (var layer in layers) {
  if (!layer.Decompress())
    throw new Exception("Unable to decompress stream.");
  byte[] data = layer.GetData();
  st.Write(data, 0, data.Length);
  layer.CompressFlate();
}
var array = ArrayAtom.FromContentStream(st.ToArray());
if (true) {
  var items = OpAtom.Find(array, new string[] { "k" });
  foreach (var pair in items) { // make red
    var args = OpAtom.GetParameters(array, pair.Item2);
    if (args != null) {
      ((NumAtom)args[0]).Real = 0;
      ((NumAtom)args[1]).Real = 1;
      ((NumAtom)args[2]).Real = 1;
      ((NumAtom)args[3]).Real = 0;
    }
  }
}
if (true) {
  var items = OpAtom.Find(array, new string[] { "rg" });
  foreach (var pair in items) { // make green
    var args = OpAtom.GetParameters(array, pair.Item2);
    if (args != null) {
      ((NumAtom)args[0]).Real = 0;
      ((NumAtom)args[1]).Real = 1;
      ((NumAtom)args[2]).Real = 0;
    }
  }
}
byte[] arrayData = array.GetData();
var so = new StreamObject(doc.ObjectSoup);
so.SetData(arrayData, 1, arrayData.Length - 2);
doc.SetInfo(page.ID, "/Contents:Del", "");
page.AddLayer(so);
doc.Save(Server.MapPath("ReplaceColors.pdf"));
```

[Visual Basic]

```vb
Using doc As New Doc()
  doc.Read(Server.MapPath("spaceshuttle.pdf"))
  doc.RemapPages(New Integer() {1, 1})
  doc.PageNumber = 2
  Dim page As Page = TryCast(doc.ObjectSoup(doc.Page), Page)
  Dim layers As StreamObject() = page.GetLayers()
  Dim st As New MemoryStream()
  For Each layer As StreamObject In layers
    If Not layer.Decompress() Then
      Throw New Exception("Unable to decompress stream.")
    End If
    Dim data As Byte() = layer.GetData()
    st.Write(data, 0, data.Length)
    layer.CompressFlate()
  Next
  Dim array As ArrayAtom = ArrayAtom.FromContentStream(st.ToArray())
  If True Then
    Dim items = OpAtom.Find(array, New String() {"k"})
    For Each pair As var In items
      ' make red
      Dim args As Atom() = OpAtom.GetParameters(array, pair.Item2)
      If args <> Nothing Then
        DirectCast(args(0), NumAtom).Real = 0
        DirectCast(args(1), NumAtom).Real = 1
        DirectCast(args(2), NumAtom).Real = 1
        DirectCast(args(3), NumAtom).Real = 0
      End If
    Next
  End If
  If True Then
    Dim items = OpAtom.Find(array, New String() {"rg"})
    For Each pair As var In items
      ' make green
      Dim args As Atom() = OpAtom.GetParameters(array, pair.Item2)
      If args <> Nothing Then
        DirectCast(args(0), NumAtom).Real = 0
        DirectCast(args(1), NumAtom).Real = 1
        DirectCast(args(2), NumAtom).Real = 0
      End If
    Next
  End If
  Dim arrayData As Byte() = array.GetData()
  Dim so As New StreamObject(doc.ObjectSoup)
  so.SetData(arrayData, 1, arrayData.Length - 2)
  doc.SetInfo(page.ID, "/Contents:Del", "")
  page.AddLayer(so)
  doc.Save(Server.MapPath("ReplaceColors.pdf"))
End Using
```

![](../../../images/pdf/ReplaceColors.pdf.png)
ReplaceColors.pdf [Page 1]

