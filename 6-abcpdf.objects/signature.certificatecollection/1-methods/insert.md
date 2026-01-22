# Insert Method

Inserts the certificate object to this collection if its value is not already present.

## Syntax

[C#]

```csharp
bool Insert(int index, X509Certificate2 cert)
```

[Visual Basic]

```vb
Function Insert(index As Integer, cert As X509Certificate2) As Boolean
```

## Params

| **Name** | **Description** |
| --- | --- |
| index | The index into this collection for insertion. |
| cert | The certificate object. |
| return | True if the certificate object is added; false if the certificate object or its value is already present. |

## Notes

This method adds the certificate object to the collection if its value is not already present.

## Example

None
