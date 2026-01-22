# Refactor Property

## Notes

Whether to eliminate redundant objects during Save.

In addition this also applies to the Append and AddImageDoc operations as these involve similar concepts.

Sometimes PDFs can contain duplicate objects. Eliminating these duplicates can reduce the size of certain PDF documents.

If this property is set to true then ABCpdf will attempt to eliminate any redundant objects. This process may require significant amounts of memory and time if the documents contain many indirect objects.

Only objects that have been loaded into memory will be considered for refactoring. This is done so that a minimal amount of time is taken to load, modify and save PDFs which should already be efficiently organized.

If you have PDFs, loading from file, which you wish to refactor, then you will need to load all the objects into memory. To do so it is sufficient to touch each of the objects using code such as the following.

[C#] for(int i = 1, n = doc.ObjectSoup.Count; i < n; i++) doc.SetInfo(i, "Touched", true); [Visual Basic] Dim n As Integer = doc.ObjectSoup.Count For i As Integer = 1 To n doc.SetInfo(i, "Touched", True) Next

## Example

None.

