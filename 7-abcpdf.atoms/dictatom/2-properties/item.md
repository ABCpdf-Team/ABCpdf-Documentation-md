---
title: "item"
css: "abcpdf-docs.css"
---

# Item Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Atom this[string name] int this[string name, int def] double this[string name, double def] string this[string name, string def] string this[string name, Enum def] ``` [Visual Basic] ``` Default Property Item(name As String) As Atom Default Property Item(name As String, def As Integer) As Integer Default Property Item(name As String, def As Double) As Double Default Property Item(>name As String, def As String) As String Default Property Item(name As String, def As Enum) As String ``` | n/a | Yes | Get or set the entry with the specified name. | 

`may throw ArgumentNullException()`

## Notes

Get or set the Atom with the specified name. In C# this property is the indexer for the class.

You can access an Atom directly or you can use one of the overloaded operators to specify numbers or strings. Using the overloads to access numbers or strings is more efficient than accessing an Atom and extracting the value from it.

You specify one of the overloads using the def parameter. If you are setting a value then this parameter is ignored. If you are getting a value then this parameter becomes the default value to be used if the underlying Atom was not the correct type. For example the default would be returned if you attempted to get an integer but the underlying Atom was actually a [StringAtom](../../stringatom/default.md).

The integer and double overload allow access to NumAtoms. The string overload allows access to StringAtom values while the Enum overload allows access to NameAtom values. Any Enum may be used and if the entry is not valid or available the string value of the Enum will be returned.

Atoms can exist in only one place at a time. If the Atom supplied is already contained by another object then a [Clone](../../1-atom/1-methods/1-clone.md) of the Atom is added.

Adding a null value will result in a [NullAtom](../../nullatom/default.md) being added to the array.

If the name is null this property throws an ArgumentNullException.

## Example

None.