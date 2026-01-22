# Resolve Function

## Syntax

[C#] IndirectObject Resolve(ObjectSoup objects) [Visual Basic] Function Resolve(objects As ObjectSoup) as IndirectObject

## Params

## Notes

This function resolves a RefAtom to the IndirectObject that it references.

If the RefAtom is referencing another RefAtom then the Resolve process will continue until an Atom which is not a RefAtom is found. If no item is found then null is returned.

## Example

None.

