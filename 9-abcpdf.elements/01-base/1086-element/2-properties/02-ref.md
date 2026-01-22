# Ref Property

## Notes

Gets any RefAtom that is part of this Element.

When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom.

If this is the case then the reference needs to be resolved through to an Atom.

This property stores the original RefAtom and the Atom property stores the resolved Atom - usually a DictAtom.

If the provided Atom is not a RefAtom then this property will be null.
