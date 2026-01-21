# Insert Function

Inserts an item into the collection at the specified position.

## Syntax

**[C#]**

```csharp
void Insert(int index, Field value)
```

**[Visual Basic]**

`Sub Insert(index As Integer, value As Field)``may throw NotSupportedException()`

## Params

| Name | Description | 
| --- | --- |
| index | The zero-based index at which value should be inserted. | 
| value | The item to insert into the array. | 

## Notes

Inserts an item into the collection at the specified position.

All Fields collections are read only so calling this function will generate a NotSupportedException.

## Example

None.