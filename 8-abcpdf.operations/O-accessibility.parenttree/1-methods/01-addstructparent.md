# AddStructParent Function

Add a new StructParent to the tree.

## Syntax

**[C#]**

```csharp
int AddStructParent(IndirectObject io, bool commit)
```

<span class=language>[Visual Basic]</span>  

            `Sub AddStructParent(io As IndirectObject, commit As bool) As Integer`
			
## Params

| Name | Description | 
| --- | --- |
| io | The object to be added. | 
| commit | Whether to commit changes to the document. | 
| return | The logical structure key for this object. | 

## Notes

Add a new StructParent to the tree.

Items are held in a cache and are not pushed through to the document until committed.

## Example

None.