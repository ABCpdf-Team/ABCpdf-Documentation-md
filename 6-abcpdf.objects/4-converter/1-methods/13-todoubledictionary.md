# ToDoubleDictionary Function

Attempts to convert a DictAtom into a Dictionary of doubles, resolving any references as necessary.

## Syntax

**[C#]**

```csharp
virtual Dictionary ToDoubleDictionary(Atom atom, double def)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ToDoubleDictionary(atom As Atom, def As double) As Dictionary`
			
## Params

| Name | Description | 
| --- | --- |
| atom | The DictAtom from which to obtain the values. | 
| def | A default value for any entries which could not be converted to the correct type. | 
| return | The dictionary. | 

## Notes

Attempts to convert a DictAtom into a Dictionary of doubles, resolving any references as necessary.

If the atom does not resolve to an DictAtom, then the return value will be null.

## Example

None.