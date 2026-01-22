# RefOrAtom Property

## Notes

Gets the Atom that was used to create this Element.

When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom.

If this is the case then the reference needs to be resolved through to an Atom.

The Ref property stores the RefAtom, if one was provided. The Atom property stores the resolved Atom.

This property will return the Ref if it is not null, or the Atom if it is.
