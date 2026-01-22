# Item(int index) Property

## Notes

Gets or sets the Element at the specified index. In C# this property is the indexer for the class.

The Item property is used to access Elements within the Array.

The ArrayAtom is accessed and used to create an Element of type T.

In the case that T has multiple sub-types, default factories will result in an item of the correct subtype being created.

The precise factory that should be used is determined at the point the ArrayElement is assigned to a property of another Element.

So since different properties may use different factories, you should not share one ArrayElement between more than one property.

Most ArrayElements cannot hold null values in a meaningful way. So in general, if you provide a null value this will result in an exception being raised.

Occasionally it is appropriate for ArrayElements to hold null values represented as NullAtoms. You can indicate this is acceptable, by setting the Nullable property.
