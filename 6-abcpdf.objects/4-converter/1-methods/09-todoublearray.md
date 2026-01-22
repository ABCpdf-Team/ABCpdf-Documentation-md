# ToDoubleArray Function

Attempts to convert an ArrayAtom into an array of doubles, resolving any references as necessary.

## Syntax

[C#]

```csharp
virtual double[] ToDoubleArray(<a href="../../../7-abcpdf.atoms/1-atom/default.htm">Atom</a> atom, double def)
```

[Visual Basic]

```vb
Overridable Function ToDoubleArray(atom As <a href="../../../7-abcpdf.atoms/1-atom/default.htm">Atom</a>, def As double) As Double[]
```

## Params

| **Name** | **Description** |
| --- | --- |
| atom | The ArrayAtom from which to obtain the values. |
| def | A default value for any entries which could not be converted to the correct type. |
| return | The array. |

## Notes

Attempts to convert an ArrayAtom into an array of doubles, resolving any references as necessary.

If the atom does not resolve to an ArrayAtom, then the return value will be null.

## Example

None
