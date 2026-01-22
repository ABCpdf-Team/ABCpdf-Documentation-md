# GetValueBool Method

Gets the Boolean value of this value converted to Boolean value using the standard JavaScript conversion.

## Syntax

[C#]

```csharp
bool GetValueBool()
```

[Visual Basic]

```vb
Function GetValueBool() As Boolean
```

## Params

| **Name** | **Description** |
| --- | --- |
| return | The Boolean value of the converted value. |

## Notes

The method is the chain of [ToJSBoolean](tojsboolean.md) and [GetBooleanBool](getbooleanbool.md) without intermediate object creation.

## Example

None
