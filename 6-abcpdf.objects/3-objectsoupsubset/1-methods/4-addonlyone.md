# AddOnlyOne  Function

## Syntax

[C#] bool AddOnlyOne(IndirectObject io) [Visual Basic] Function AddOnlyOne(io As IndirectObject) As Boolean

may throw Exception()

## Params

## Notes

Add a parent object ignoring any objects it may refer to.

If the item was added this function returns true. If the item was not added because the subset already contained it or because the RemapTypes specified a different remapping then the function returns false.

If the specified object is not part of the soup specified in the ObjectSoupSubset constructor then an exception will be raised.

## Example

None.

