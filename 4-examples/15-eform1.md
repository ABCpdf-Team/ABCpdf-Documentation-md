# eForm Fields Example

## Src

First we create an ABCpdf Doc object and read in our template form.

[C#] using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/form.pdf")); doc.Form.NeedAppearances = false; // for PDF 2.0 [Visual Basic] Using doc As New Doc() doc.Read(Server.MapPath("../mypics/form.pdf")) doc.Form.NeedAppearances = False ' for PDF 2.0

## Add

We iterate through each of the top level fields. For each field we set the value of the field to be equal to the value of the name.

[C#] string[] names = doc.Form.GetFieldNames(); foreach (string theName in names) { var field = doc.Form[theName]; field.Value = field.Name; } [Visual Basic] Dim theNames As String() = doc.Form.GetFieldNames() For Each theName As String In theNames Dim theField As Field = doc.Form(theName) theField.Value = theField.Name Next

## Save

Finally we save.

[C#] doc.Save(Server.MapPath("eformfields.pdf")); [Visual Basic] doc.Save(Server.MapPath("eformfields.pdf")) End Using

## Results

Given the following document.

form.pdf

This is the kind of output you might expect.

eformfields.pdf

