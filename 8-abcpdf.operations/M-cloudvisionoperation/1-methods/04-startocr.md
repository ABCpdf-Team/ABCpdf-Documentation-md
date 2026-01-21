# StartOcr Function

Start OCR operation on the pages that have been added.

## Syntax

**[C#]**

```csharp
void StartOcr()
```

<span class=language>[Visual Basic]</span>  

            `Function StartOcr()`
			
## Params

| Name | Description | 
| --- | --- |
| none |  | 

## Notes

Start OCR operation on the pages that have been added.
            
## Example

Here we read a TIFF into a Doc, OCR it and then save the PDF.

The text in this document is indivisible which means you can select and copy it, but it does not obscure the image in the background.

To run this code you will need to replace the Google API key with one of your own.

[C#]

```csharp
string theSrc = Server.MapPath("mypics/multipage.tif");
string theDst = Server.MapPath("CloudOCR.pdf");
using (Doc doc = new Doc()) {
  doc.Read(theSrc);

  var op = new CloudVisionOperation(doc);
  op.AddPages();
  op.ApiKey = "AIzAUlBcTPDwxUNn5uQvSHONpsTpAqVJHbfOa";
  op.StartOcr();
  op.WaitAll();
  doc.Save(theDst);
}
```

<span class=language>[Visual
    Basic]</span>
```vbnet
Dim theSrc As String = Server.MapPath("mypics/multipage.tif")
Dim theDst As String = Server.MapPath("CloudOCR.pdf")
Using doc As New Doc()
  doc.Read(theSrc)

  Dim op As New CloudVisionOperation(doc)
  op.AddPages()
  op.ApiKey = "AIzAUlBcTPDwxUNn5uQvSHONpsTpAqVJHbfOa"  op.StartOcr()  op.WaitAll()

  doc.Save(theDst)
End Using
```