# Convert Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Converter ``` [Visual Basic] `Converter` | n/a | Yes | A Converter for the document. | 

## Notes

A [Converter](../../4-converter/default.md) for the document.

The Converter can be used for the resolution and extraction of atomic data held within the document.

Because the Converter has direct access to the raw data it can be significantly faster than resolving Atoms directly. This is especially the case for accessing collections such as arrays or dictionaries of data.

It is very simple to use. For example to get all the character widths from a font you might use code of the following form.

[C#]

```csharp
Atom atom = Atom.GetItem(font.Atom, "Widths");
double[] widths = doc.ObjectSoup.Convert.ToDoubleArray(atom, 1000);
```

**[Visual Basic]**

```vbnet
Dim atom As Atom = Atom.GetItem(font.Atom, "Widths")
Dim widths As Double() = doc.ObjectSoup.Convert.ToDoubleArray(atom, 1000)
```

## Example

None.