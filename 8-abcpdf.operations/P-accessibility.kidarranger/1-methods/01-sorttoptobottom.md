# SortTopToBottom Function

Sort the kids of the parent element so that they go in order from the top to the bottom.

## Syntax

**[C#]**

```csharp
static void SortTopToBottom(Structure structure, StructureElementElement parent, List areas)
```

<span class=language>[Visual Basic]</span>  

            `Shared Function SortTopToBottom(structure As Structure, parent As StructureElementElement, areas As List)`
			
## Params

| Name | Description | 
| --- | --- |
| structure | The structure to operate on. | 
| parent | The parent whos kids need sorting. | 
| areas | A set of sub-areas. This value may be null. | 

## Notes

Sort the kids of the parent element so that they go in order from the top to the bottom.

You can separate each page into sub-areas which will be sorted separately.

In this way you can sort multiple columns or rows independently.

## Example

None.