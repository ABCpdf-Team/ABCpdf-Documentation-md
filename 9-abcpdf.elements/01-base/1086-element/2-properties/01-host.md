# Host Property

## Notes

Gets the host IndirectObject.

The host is specified during construction or in a later call to Assign.

The host is primarily used to indicate the document to which the Element belongs.

As such it can be any IndirectObject in the document.

However it is often useful to choose one which is closely associated with the Atom provided.

For example, if you create an Element from an IndirectObject, the Host can be itself.
