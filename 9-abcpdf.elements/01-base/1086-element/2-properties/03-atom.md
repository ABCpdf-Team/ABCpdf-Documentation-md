# Atom Property

## Notes

Gets any Atom that is part of this Element.

When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom.

If this is the case then the reference needs to be resolved through to an Atom.

This property stores the resolved Atom - usually a DictAtom but occasionally other types for some specific types of Element.

However this property will never be a RefAtom as all references have been resolved.
