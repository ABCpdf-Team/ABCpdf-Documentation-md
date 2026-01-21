# ToInt32Array Function

Attempts to convert an ArrayAtom into an array of ints, resolving any references as necessary.

## Syntax

**[C#]**

```csharp
virtual int[] ToInt32Array(Atom atom, int def)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ToInt32Array(atom As Atom, def As int) As Integer[]`
			
## Params

| Name | Description | 
| --- | --- |
| atom | The ArrayAtom from which to obtain the values. | 
| def | A default value for any entries which could not be converted to the correct type. | 
| return | The array. | 

## Notes

Attempts to convert an ArrayAtom into an array of ints, resolving any references as necessary.

If the atom does not resolve to an ArrayAtom, then the return value will be null.

## Example

None.