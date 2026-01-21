# Add Function

Add an item to the dictionary.

## Syntax

**[C#]**

```csharp
void Add(string key, Atom atm)
void Add(string key, int num)
void Add(string key, double real)
void Add(string key, string str)
```

**[Visual Basic]**

```
Sub Add(key As String, atm As Atom)
Sub Add(key As String, num As Integer)
Sub Add(key As String, real As Double)
Sub Add(key As String, str As String)
```
`may throw ArgumentException()` `may throw ArgumentNullException()`

## Params

| Name | Description | 
| --- | --- |
| key | The string to use as the key of the element to add. | 
| atm | The Atom to be added. | 
| num | The integer to be added. | 
| real | The floating point value to be added. | 
| str | The string to be added. | 

## Notes

This method adds an item to the dictionary.

You can add an Atom directly into the dictionary or you can use one of the overloaded operators to add numbers or strings.

When you add a string this is encapsulated within a [StringAtom](../../stringatom/default.md) and then inserted. When you add an integer or floating point value this is converted to a [NumAtom](../../numatom/default.md) and then inserted. These operations are more efficient than creating an Atom and adding it yourself.

Atoms can exist in only one place at a time. If the Atom supplied is already contained by another object then a [Clone](../../1-atom/1-methods/1-clone.md) of the Atom is added.

Adding a null value will result in a [NullAtom](../../nullatom/default.md) being added to the dictionary.

If the key is null then this method will throw an ArgumentNullException. If the key is already present in the dictionary then this method will throw an ArgumentException.

## Example

None.