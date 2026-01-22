# eForm Stamp Example

## Src

First we create an ABCpdf Doc object and read in our template form.

[C#] using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/form.pdf")); doc.Form.NeedAppearances = false; // for PDF 2.0 doc.Font = doc.AddFont("Helvetica-Bold"); [Visual Basic] Using doc As New Doc() doc.Read(Server.MapPath("../mypics/form.pdf")) doc.Form.NeedAppearances = False ' for PDF 2.0 doc.Font = doc.AddFont("Helvetica-Bold")

## Add

We set the values of selected fields and then we stamp all field values into the document.

[C#] doc.Form["Day"].Value = "23"; doc.Form["Month"].Value = "February"; doc.Form["Year"].Value = "2005"; doc.Form["State"].Value = "Arizona"; doc.Form.Stamp(); [Visual Basic] doc.Form("Day").Value = "23" doc.Form("Month").Value = "February" doc.Form("Year").Value = "2005" doc.Form("State").Value = "Arizona" doc.Form.Stamp()

## Save

Finally we save.

[C#] doc.Save(Server.MapPath("eformstamp.pdf")); [Visual Basic] doc.Save(Server.MapPath("eformstamp.pdf")) End Using

## Results

Given the following document.

form.pdf

This is the kind of output you might expect.

eformstamp.pdf

