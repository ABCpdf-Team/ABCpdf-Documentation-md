# CreateObject Method

Creates a JavaScript object.

## Syntax

[C#]

```csharp
JSValue CreateObject()
```

[Visual Basic]

```vb
Function CreateObject() As JSValue
```

## Params

| **Name** | **Description** |
| --- | --- |
| return | A new JavaScript object. |

## Notes

The method creates a JavaScript object. It is much better than calling [ConvertToJS](converttojs.md) with an empty array of KeyValuePair<string, object>.

## Example

None
