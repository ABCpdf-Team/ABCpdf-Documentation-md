# ToInt32Dictionary Function

Attempts to convert a DictAtom into a Dictionary of ints, resolving any references as necessary.

## Syntax

**[C#]**

```csharp
virtual Dictionary ToInt32Dictionary(Atom atom, int def)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ToInt32Dictionary(atom As Atom, def As int) As Dictionary`
			
## Params

| Name | Description | 
| --- | --- |
| atom | The DictAtom from which to obtain the values. | 
| def | A default value for any entries which could not be converted to the correct type. | 
| return | The dictionary. | 

## Notes

Attempts to convert a DictAtom into a Dictionary of ints, resolving any references as necessary.

If the atom does not resolve to an DictAtom, then the return value will be null.

## Example

None.