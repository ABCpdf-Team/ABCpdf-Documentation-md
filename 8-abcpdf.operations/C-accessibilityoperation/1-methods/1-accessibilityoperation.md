---
title: "1-accessibilityoperation"
css: "abcpdf-docs.css"
---

# AccessibilityOperation Constructor

AccessibilityOperation Constructor.

## Syntax

**[C#]**

```csharp
AccessibilityOperation(Doc doc)
```

<span class=language>[Visual
            Basic]</span>  
`Sub New(doc As Doc)``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| doc | The PDF Document | 

## Notes

Create an AccessibilityOperation for accessibility. If the doc is null then an exception will be raised.

## Example

Here we read an existing PDF and make it accessible.

We produce output conformant to the PDF specification and compliant with use within Acrobat. However please note that Accessibility is not well supported outside Acrobat.

In particular some versions of software such as NVDAccess do not necessarily handle all constructs correctly. In particular they have problems with form XObjects and so one needs to avoid this type of construct.

The code below calls Page.StampFormXObjects on all pages in the document to ensure that all form XObjects are removed before the document is made accessible.

The process of stamping form XObjects will not normally make much difference. However in some cases you may find there is a level of expansion in size and very occasionally you may see subtle differences in transparency blending. Nevertheless if you want compatibility, there is no other choice.

[C#]

```csharp
using var doc = new Doc();
doc.Read(Server.MapPath("spaceshuttle.pdf"));
var pages = doc.ObjectSoup.Catalog.Pages.GetPageArrayAll();
foreach (var page in pages)
  page.StampFormXObjects(true); // see notes on NVDA above
var op = new AccessibilityOperation(doc);
op.PageContents.AddPages();
op.MakeAccessible();
doc.Save(Server.MapPath("accessible.pdf"));
```

[Visual Basic]

```vbnet
Using doc As New Doc()
  doc.Read(Server.MapPath("spaceshuttle.pdf"))
  Dim pages As Page() = doc.ObjectSoup.Catalog.Pages.GetPageArrayAll()
  For Each page As Page In pages
    page.StampFormXObjects(True)
  Next
  ' see notes on NVDA above
  Dim op As New AccessibilityOperation(doc)
  op.PageContents.AddPages()
  op.MakeAccessible()
  doc.Save(Server.MapPath("accessible.pdf"))
End Using
```