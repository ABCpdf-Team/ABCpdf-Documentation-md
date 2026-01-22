# Item(TKey key) Property

## Notes

Gets or sets the value associated with the specified key. In C# this property is the indexer for the class.

The Item property is used to access Elements within the tree.

The tree is searched for a matching entry and used to create an Element of type T.

Note that no factories are used here so the element will always be type T - not a subclass.

Trees cannot hold null values in a meaningful way. So if you provide a null value, this will result in an exception being raised.

If the specified key is not found, a get operation throws a KeyNotFoundException, and a set operation creates a new element with the specified key.
