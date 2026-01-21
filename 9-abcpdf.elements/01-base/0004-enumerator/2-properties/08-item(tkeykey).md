# Item(TKey key) Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp TVal ``` [Visual Basic] `TVal` | null | No | Gets or sets the value associated with the specified key. | 

`KeyNotFoundException: Thrown if getting an item, but the specified key was not found. NullReferenceException: Thrown if an attempt is made to assign a null value.`

## Notes

Gets or sets the value associated with the specified key. In C# this property is the indexer for the class.

The Item property is used to access [Elements](../../1086-element/default.md) within the tree.

The tree is searched for a matching entry and used to create an [Element](../../1086-element/default.md) of type T.

Note that no factories are used here so the element will always be type T - not a subclass.

Trees cannot hold null values in a meaningful way. So if you provide a null value, this will result in an exception being raised.

If the specified key is not found, a get operation throws a KeyNotFoundException, and a set operation creates a new element with the specified key.

## Example

None.