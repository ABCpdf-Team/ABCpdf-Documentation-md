# Root Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | Yes | The root catalog object. | 

## Notes

This property holds the ID of the catalog object.

The catalog is the root of the whole PDF document. It contains information on the root Pages object and the Outline object.

For dynamically created documents the root of the document is always one. However documents read from existing PDF files may use different root IDs.

## Example

The following code snippet illustrates how one might find some information about a PDF document.

[C#]

```csharp
using var doc = new Doc();
doc.Read(Server.MapPath("../mypics/mydoc.pdf"));
string vers = doc.GetInfo(doc.Root, "Version");
string names = doc.GetInfo(doc.Root, "/Names");
string pages = doc.GetInfo(doc.Root, "pages");
string outlines = doc.GetInfo(doc.Root, "outlines");
Response.Write($"Version {vers}&lt;br&gt;");
Response.Write($"Names {names}&lt;br&gt;");
Response.Write($"Pages ID {pages}&lt;br&gt;");
Response.Write($"Outlines ID {outlines}&lt;br&gt;");
```

**[Visual Basic]**

```vbnet
Using doc As New Doc()
  doc.Read(Server.MapPath("../mypics/mydoc.pdf"))
  Dim theVers As String, theNames As String, thePages As String, theOutlines As String
  theVers = doc.GetInfo(doc.Root, "Version")
  theNames = doc.GetInfo(doc.Root, "/Names")
  thePages = doc.GetInfo(doc.Root, "pages")
  theOutlines = doc.GetInfo(doc.Root, "outlines")
  Response.Write($"Version {theVers}&lt;br&gt;")
  Response.Write($"Names {theNames}&lt;br&gt;")
  Response.Write($"Pages ID {thePages}&lt;br&gt;")
  Response.Write($"Outlines ID {theOutlines}&lt;br&gt;")
End Using
```

This might result in the following output.

Version /1.4 Names 12 0 R Pages ID 618 Outlines ID 2169