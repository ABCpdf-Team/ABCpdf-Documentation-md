# Insert Function

Inserts an object into the Soup at the specified position.

## Syntax

**[C#]**

```csharp
void Insert(int index, IndirectObject value)
```

**[Visual Basic]**

`Sub Insert(index As Integer, value As IndirectObject)``may throw NotSupportedException()`

## Params

| Name | Description | 
| --- | --- |
| index | The zero-based index at which value should be inserted. | 
| return | The Object to insert into the Soup. | 

## Notes

Objects within a collection refer to each other by index. This means that once an object is inserted into the Soup it must stay at the same index. If it moves then references may be broken.

Insertion at a particular position might require other objects to be moved. For this reason this method always throws a NotSupportedException.

## Example

None.