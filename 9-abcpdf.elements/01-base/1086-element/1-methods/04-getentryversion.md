# GetEntryVersion Function

Get the minimum PDF version required for the use of a particular named entry.

## Syntax

[C#]

```csharp
virtual PDFVersion GetEntryVersion(string entry)
```

[Visual Basic]

```vb
Overridable Function GetEntryVersion(entry As string) As PDFVersion
```

## Params

| **Name** | **Description** |
| --- | --- |
| entry | The name of the entry. |
| return | The PDF version. |

## Notes

Get the minimum PDF version required for the use of a particular named entry.

This function should be overridden by classes which inherit from this.

They should provide return values for the entries specific to the new class.
