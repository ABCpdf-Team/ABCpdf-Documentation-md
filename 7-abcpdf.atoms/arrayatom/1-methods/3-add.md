# Add Function

Add an item to the end of the array.

## Syntax

**[C#]**

```csharp
int Add(Atom atm)
int Add(int num)
int Add(double real)
int Add(string str)
```

**[Visual Basic]**

```
Function Add(atm As Atom) As Integer
Function Add(num As Integer) As Integer
Function Add(real As Double) As Integer
Function Add(str As String) As Integer
```

## Params

| Name | Description | 
| --- | --- |
| atm | The Atom to be added. | 
| num | The integer to be added. | 
| real | The floating point value to be added. | 
| str | The string to be added. | 
| return | The position in which the new element was inserted. | 

## Notes

This method adds an item to the array.

You can add an Atom directly into the array or you can use one of the overloaded operators to add numbers or strings.

When you add a string this is encapsulated within a [StringAtom](../../stringatom/default.md) and then inserted. When you add an integer or floating point value this is converted to a [NumAtom](../../numatom/default.md) and then inserted. These operations are more efficient than creating an Atom and adding it yourself.

Atoms can exist in only one place at a time. If the Atom supplied is already contained by another object then a [Clone](../../1-atom/1-methods/1-clone.md) of the Atom is added.

Adding a null value will result in a [NullAtom](../../nullatom/default.md) being added to the array.

## Example

None.