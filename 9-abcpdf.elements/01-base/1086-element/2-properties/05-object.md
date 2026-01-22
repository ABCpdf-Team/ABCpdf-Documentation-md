# Object Property

## Notes

Gets the IndirectObject that is part of this Element.

When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom.

If this is the case then this property stores the referenced IndirectObject.

If the provided Atom is not a RefAtom then this property will be null.
