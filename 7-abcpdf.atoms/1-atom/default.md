# Atom Class

A PDF atomic object comprising a basic chunk of PDF data.

If you are going to be using Atoms then you will want to download the [Adobe PDF Specification](http://partners.adobe.com/). This document explains the names and types that can be used and how they are interpreted.

Common Operations.

Get a named property from the dictionary of an IndirectObject. In the example below we use the Type property which is typically a name but the principles are similar for other entries of other types:

**[C#]**

</p>
```csharp
NameAtom type = io.Resolve(Atom.GetItem(io.Atom, "Type")) as NameAtom;
```

**[Visual Basic]**

```vbnet
Dim type As NameAtom = io.Resolve(Atom.GetItem(io.Atom, "Type"))
```

Get an value out of an array atom. In the the event that the atom is not an array or does not have sufficient entries then the return value will be null. In the example below we are looking for entry two - this is the third entry since entries are zero based:

[C#]

```csharp
NumAtom num = io.Resolve(Atom.GetItem(atom, 2)) as NumAtom;
```

**[Visual Basic]**

```vbnet
Dim num As NumAtom = io.Resolve(Atom.GetItem(atom, 2))
```

Get a stream referenced from a property of an IndirectObject. In the example below we use the FontFile2 property (a reference to an embedded TrueType font):

[C#]

```csharp
StreamObject stream = io.ResolveObj(Atom.GetItem(io.Atom, "FontFile2")) as StreamObject;
```

**[Visual Basic]**

```vbnet
Dim stream As StreamObject = io.ResolveObj(Atom.GetItem(io.Atom, "FontFile2"))
```

Add a named entry to an IndirectObject. In the example below we add a V entry which is a string. We keep the returned StringAtom so we can manipulate the value:

[C#]

```csharp
StringAtom str = (StringAtom)Atom.SetItem(io.Atom, "V", new StringAtom());
```

**[Visual Basic]**

```vbnet
Dim str As StringAtom = Atom.SetItem(io.Atom, "V", New StringAtom())
```

Add a named entry to an IndirectObject. In the example below we add an array entry to specify a border array. Rather than creating an ArrayAtom and specifying the individual values we just specify the raw string value of the object:

[C#]

```csharp
Atom.SetItem(io.Atom, "Border", Atom.FromString("[ 0 0 1 ]"));
```

**[Visual Basic]**

```vbnet
Atom.SetItem(io.Atom, "Border", Atom.FromString("[ 0 0 1 ]"))
```

<p>
```
System.Object
 WebSupergoo.ABCpdf13.Atoms.Atom
 WebSupergoo.ABCpdf13.Atoms.ArrayAtom
 WebSupergoo.ABCpdf13.Atoms.BoolAtom
 WebSupergoo.ABCpdf13.Atoms.DictAtom
 WebSupergoo.ABCpdf13.Atoms.NameAtom
 WebSupergoo.ABCpdf13.Atoms.NullAtom
 WebSupergoo.ABCpdf13.Atoms.NumAtom
 WebSupergoo.ABCpdf13.Atoms.RefAtom
 WebSupergoo.ABCpdf13.Atoms.OpAtom
 WebSupergoo.ABCpdf13.Atoms.StringAtom

Implements: ICloneable, IDisposable, IEquatable, IComparable
```

## Method Description S&raquo;&nbsp; FromString Create an appropriate type of Atom from a raw PDF string representation. S&raquo;&nbsp; GetBool Gets the Boolean value from the Atom if it is a BoolAtom. S&raquo;&nbsp; GetDouble Gets the double value from the Atom if it is a NumAtom. S&raquo;&nbsp; GetID Gets the Object ID value from the Atom if it is a RefAtom. S&raquo;&nbsp; GetInt Gets the integer value from the Atom if it is a NumAtom. S&raquo;&nbsp; GetItem Gets the specified item from the Atom if it is of a type which contains other Atoms. S&raquo;&nbsp; GetName Gets the Name value from the Atom if it is a NameAtom. S&raquo;&nbsp; GetText Gets the Text value from the Atom if it is a StringAtom. S&raquo;&nbsp; RemoveItem Removes the named entry from the Atom if it is a DictAtom. S&raquo;&nbsp; SetItem Adds a specified item to the Atom if it is of a type which contains other Atoms. GetData The byte array representation of the Atom as it would appear in a PDF. Clone Creates a deep copy of the current Atom. Dispose Dispose of the object. Equals Test whether the two Atoms are the same. GetHashCode A hash code for the Atom. ToString The string representation of the Atom as it would appear in a PDF. &nbsp;

## Property Description none &nbsp;