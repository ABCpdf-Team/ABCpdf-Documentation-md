# Item(string key) Property

## Notes

Gets or sets the Element at the specified index. In C# this property is the indexer for the class.

The Item property is used to access Elements within the dictionary.

The DictAtom is accessed and used to create an Element of type T.

In the case that T has multiple sub-types, default factories will result in an item of the correct subtype being created.

The precise factory that should be used is determined at the point the DictElement is assigned to a property of another Element.

So since different properties may use different factories, you should not share one DictElement between more than one property.

DictElements cannot hold null values in a meaningful way. So if you provide a null value, this will result in an exception being raised.

If the specified key is not found, a get operation throws a KeyNotFoundException, and a set operation creates a new element with the specified key.
