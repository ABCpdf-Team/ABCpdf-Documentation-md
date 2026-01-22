# Adopt Method

Adopt a specified Bookmark.

## Syntax

[C#]

```csharp
void Adopt(<a href="../default.htm">Bookmark</a> value)
```

[Visual Basic]

```vb
Sub Adopt(value As <a href="../default.htm">Bookmark</a>)
```

## Params

| **Name** | **Description** |
| --- | --- |
| value | The bookmark to be adopted. |

## Notes

Use this method to move bookmarks within the bookmark hierarchy.

The bookmark to be adopted is detached from the bookmark hierarchy. Then it is added at the end of the bookmark collection for the current object.

Some Adopt operations are not possible. For example a child cannot adopt its parent. In these cases the field structure will be left unchanged and an exception thrown.

## Example

None
