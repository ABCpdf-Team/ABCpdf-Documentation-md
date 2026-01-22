# AddFamily Function

## Syntax

[C#] int AddFamily(IndirectObject parent) int AddFamily(DictAtom dict) [Visual Basic] Function AddFamily(parent As IndirectObject) As Integer Function AddFamily(dict As DictAtom) As Integer

may throw Exception()

## Params

## Notes

Add a parent object along with all objects it refers to.

If a dictionary is specified there is no parent. In this situation only the objects referred to in the dictionary will be added.

If the parent or dictionary is not part of the soup specified in the ObjectSoupSubset constructor then an exception will be raised.

## Example

None.

