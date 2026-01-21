# AddDocTimestamp Function

Adds a Signature field compatible with a DocTimeStamp.

## Syntax

**[C#]**

```csharp
Signature AddDocTimestamp()
Signature AddDocTimestamp(string name)
```

<span class=language>[Visual Basic]</span>  

```
Function AddDocTimestamp() As Signature
Function AddDocTimestamp(name As string) As Signature
```

## Params

| Name | Description | 
| --- | --- |
| name | The name of the document timestamp field. If no name is specified a unique name will be added. | 

## Notes

Adds a Signature field compatible with a document timestamp.

Add an RFC 3161 compliant document timestamp field to the form.

To sign the timestamp you need to specify either a TimestampServiceUrl or a CustomSigner and then call Timestamp.

## Example

See the Annotations example project for a full example.

However the following is a code snippet showing how this might be used.

[C#]

```csharp
using var doc = new Doc();
// ... set up the doc perhaps by reading a PDF
if (doc.PageCount == 0)
  doc.Page = doc.AddPage();
var sig = doc.Form.AddDocTimestamp("Timestamp");
var uri = new Uri("http://timestamp.digicert.com");
var oid = new Oid(CryptoConfig.MapNameToOID("SHA256"));
sig.TimestampServiceUrl = uri;
sig.Timestamp(oid, 0);
```

**[Visual Basic]**

```vbnet
Dim doc = New Doc()
' ... set up the doc perhaps by reading a PDF
If doc.PageCount = 0 Then
  doc.Page = doc.AddPage()
End If
Dim sig = doc.Form.AddDocTimestamp("Timestamp")
Dim uri As New Uri("http://timestamp.digicert.com")
Dim oid As New Oid(CryptoConfig.MapNameToOID("SHA256"))
sig.TimestampServiceUrl = uri
sig.Timestamp(oid, 0)
```