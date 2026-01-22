# GetData Function

Get the conforming document as raw data.

## Syntax

[C#]

```csharp
byte[] GetData(Doc doc)
```

[Visual Basic]

```vb
Function GetData(doc As Doc) As Byte()
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | The document. |
| return | The PDF document as an array of bytes. |

## Notes

The method writes the document in a conforming PDF format according to the [Conformance](2-properties/conformance.md) property. Any conformance error is reported in the [Errors](2-properties/errors.md) property after the method finishes.

## Example

None
