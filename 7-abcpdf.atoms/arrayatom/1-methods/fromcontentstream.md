---
title: "fromcontentstream"
css: "abcpdf-docs.css"
---

|  |  | FromContentStream Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create an array of Atoms from a byte array containing a sequence of PDF objects |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static ArrayAtom FromContentStream(string text) static ArrayAtom FromContentStream(byte[] data) static ArrayAtom FromContentStream(byte[] value, out IList offsets) ``` [Visual Basic] ``` Shared Function FromContentStream(text As String) As ArrayAtom Shared Function FromContentStream(data() As Byte) As ArrayAtom Shared Function FromContentStream(data() As Byte, Out IList offsets) As ArrayAtom ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | A string holding a sequence of atoms. | 
| data | A chunk of data holding the sequence of atoms. | 
| offsets | The byte offsets in the data for the start each of atom in the returned array. | 
| return | An ArrayAtom holding the atoms in the content stream. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create an array of Atoms from a byte array containing a sequence of PDF objects. This method is useful for deconstructing PDF content streams for analysis and modification. To convert back into a content stream you can use the Atom.GetData function. The returned offsets relate to the byte offsets for the start of each atom in the array that is returned. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This example shows how to use the FromContentStream function to parse and display a PDF content stream. [C#] ```csharp var sb = new StringBuilder(); using (var doc = new Doc()) { doc.Read(Server.MapPath("spaceshuttle.pdf")); var page = doc.ObjectSoup[doc.Page] as Page; var array = ArrayAtom.FromContentStream(page.GetContentData()); int indent = 0; var indentPlus = new HashSet(new string[] { "q", "BT" }); var indentMinus = new HashSet(new string[] { "Q", "ET" }); var items = OpAtom.Find(array); int index = 0; foreach (var pair in items) { string op = ((OpAtom)array[pair.Item2]).Text; // add indent to code if (indentMinus.Contains(op)) indent--; for (int i = 0; i [Visual Basic] ```vbnet Dim sb As New StringBuilder() Using doc As New Doc() doc.Read(Server.MapPath("spaceshuttle.pdf")) Dim page As Page = TryCast(doc.ObjectSoup(doc.Page), Page) Dim array As ArrayAtom = ArrayAtom.FromContentStream(page.GetContentData()) Dim indent As Integer = 0 Dim indentPlus As New HashSet(Of String)(New String() {"q", "BT"}) Dim indentMinus As New HashSet(Of String)(New String() {"Q", "ET"}) Dim items As IList(Of Tuple(Of String, Integer)) = OpAtom.Find(array) Dim index As Integer = 0 For Each pair As var In items Dim op As String = DirectCast(array(pair.Item2), OpAtom).Text ' add indent to code If indentMinus.Contains(op) Then System.Math.Max(System.Threading.Interlocked.Decrement(indent),indent + 1) End If Dim i As Integer = 0 While i index Then sb.Append(" ") End If Dim item As Atom = array(i) ' we write arrays out individually so that ' we can override default cr lf behavior Dim itemArray As ArrayAtom = TryCast(item, ArrayAtom) If itemArray <> Nothing Then Dim n As Integer = itemArray.Count sb.Append("[") Dim j As Integer = 0 While j n - 1 Then sb.Append(" ") End If System.Math.Max(System.Threading.Interlocked.Increment(j),j - 1) End While sb.Append("]") Else sb.Append(item.ToString()) End If System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While sb.AppendLine() If indentPlus.Contains(op) Then System.Math.Max(System.Threading.Interlocked.Increment(indent),indent - 1) End If index = pair.Item2 + 1 Next ' write out any atoms that are left over Dim i As Integer = index While i PageContents.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>