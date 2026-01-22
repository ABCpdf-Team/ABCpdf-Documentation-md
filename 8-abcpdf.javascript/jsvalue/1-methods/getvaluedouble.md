# GetValueDouble Method

Gets the Double value of this value converted to number using the standard JavaScript conversion.

## Syntax

[C#]

```csharp
double GetValueDouble()
```

[Visual Basic]

```vb
Function GetValueDouble() As Double
```

## Params

| **Name** | **Description** |
| --- | --- |
| return | The Double value of the converted value. |

## Notes

The method is the chain of [ToJSNumber](tojsnumber.md) and [GetNumberDouble](getnumberdouble.md) without intermediate object creation.

## Example

None
