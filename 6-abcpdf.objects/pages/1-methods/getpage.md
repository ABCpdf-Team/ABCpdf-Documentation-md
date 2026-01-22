# GetPage Function

Performs a fast lookup to retrieve a particular Page from this node tree

## Syntax

[C#]

```csharp
<a href="../../page/default.htm">Page</a> GetPage(int page)
```

[Visual Basic]

```vb
Function GetPage(Integer page) As <a href="../../page/default.htm">Page</a>
```

## Params

| **Name** | **Description** |
| --- | --- |
| page | The page number - a one based index |
| returns | The specified Page object or null if one could not be found. |

## Notes

Performs a fast lookup to retrieve a particular Page from this node tree.

The page is specified in terms of the index of the page within the tree. This is a one-based index within the current Pages node. Since a Pages node relates to only a portion of a PDF document, the page number within the Pages node is offset from the page number within the document.

## Example

None
