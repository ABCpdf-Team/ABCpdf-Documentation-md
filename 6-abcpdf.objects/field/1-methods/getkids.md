# GetKids Function

Gets a set of Fields that are descendents of this one.

## Syntax

[C#]

```csharp
<a href="../default.htm">Field</a>[] GetKids(int maximumDepth)
```

[Visual Basic]

```vb
Function GetKids(maximumDepth As Integer) As <a href="../default.htm">Field</a>()
```

## Params

| **Name** | **Description** |
| --- | --- |
| maximumDepth | The maximum depth to search. |

## Notes

Gets a set of Fields that are descendents of this one.

The maximum depth parameter allows you to control the depth to which the field tree is searched. One for immediate children, two for children and grandchildren, etc.

Set the maximumDepth to Int32.MaxValue if you wish to retrieve all the fields under this one.

## Example

None
