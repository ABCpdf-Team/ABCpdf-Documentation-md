# Load Function

Loads the file trailer data.

## Syntax

**[C#]**

```csharp
void Load(ObjectSoup soup)
```

<span class=language>[Visual Basic]</span>  

            `Function Load(soup As ObjectSoup)`
			
## Params

| Name | Description | 
| --- | --- |
| soup | The ObjectSoup of a Doc object. The Doc must have been loaded using Doc.Read. | 

## Notes

Loads the file trailer data.

## Example

The following code tests to see if any of the revisions in a document are hybrid.

[C#]

```csharp
bool isHybrid = false;
using var doc = new Doc();
doc.Read(Server.MapPath("../mypics/sample.pdf"));
using (var eof = new ObjectSoup.Eof()) {
  eof.Load(doc.ObjectSoup);
  var xref = eof.XRef;
  while (xref != null) {
    if (xref.Type == ObjectSoup.XRefType.Hybrid) {
      isHybrid = true;
      break;
    }
    xref = xref.Prev;
  }
}
// do something with isHybrid
```

<span class=language>[Visual Basic]</span>
```vbnet
Dim isHybrid As Boolean = False
Using doc = New Doc()
  doc.Read(Server.MapPath("../mypics/sample.pdf"))
  Using eof = New ObjectSoup.Eof()
    eof.Load(doc.ObjectSoup)
    Dim xref = eof.XRef
    While xref <> Nothing
      If xref.Type = ObjectSoup.XRefType.Hybrid Then
        isHybrid = True
        Exit While
      End If
      xref = xref.Prev
    End While
    ' do something with isHybrid
  End Using
End Using
```