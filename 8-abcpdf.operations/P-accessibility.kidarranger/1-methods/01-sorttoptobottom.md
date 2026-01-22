# SortTopToBottom Function

Sort the kids of the parent element so that they go in order from the top to the bottom.

## Syntax

[C#]

```csharp
static void SortTopToBottom(<a href="../../N-accessibility.structure/default.htm">Structure</a> structure, StructureElementElement parent, List&lt;XRect&gt; areas)
```

[Visual Basic]

```vb
Shared Function SortTopToBottom(structure As <a href="../../N-accessibility.structure/default.htm">Structure</a>, parent As StructureElementElement, areas As List&lt;XRect&gt;)
```

## Params

| **Name** | **Description** |
| --- | --- |
| structure | The structure to operate on. |
| parent | The parent whos kids need sorting. |
| areas | A set of sub-areas. This value may be null. |

## Notes

Sort the kids of the parent element so that they go in order from the top to the bottom.

You can separate each page into sub-areas which will be sorted separately.

In this way you can sort multiple columns or rows independently.

## Example

None
