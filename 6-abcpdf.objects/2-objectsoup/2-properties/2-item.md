# Item Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IndirectObject this[int index] ``` [Visual Basic] `Default Property Item(index As Integer) As IndirectObject` | n/a | No | Gets or sets the object at the specified index. | 

`may throw ArgumentOutOfRangeException()`

## Notes

Gets or sets the IndirectObject at the specified index. In C# this property is the indexer for the class.

An IndirectObject can exist in only one ObjectSoup at a time. If the object supplied is already contained in another ObjectSoup then a Clone of the object is inserted.

When an IndirectObject is inserted the [ID](../../1-indirectobject/2-properties/1-id.md) is updated to reflect the position of the object within the Soup.

## Example

None.