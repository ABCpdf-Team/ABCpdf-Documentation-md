# Resolve Function

## Syntax

[C#] Atom Resolve(Atom atom)

## Params

## Notes

Atoms come in two basic types. Data atoms like NumAtoms and NameAtoms contain actual data. RefAtoms contain a reference to an IndirectObject which contains another Atom.

Quite often you will want to resolve any RefAtoms and just obtain the Atom within the final IndirectObject - you want the final item of data rather than a reference to a piece of data.

This function takes an Atom. If it is a RefAtom it finds the Atom to which it points. It keeps doing this until it finds and returns the final data Atom in the chain.

This method may return null if null is passed in, if a RefAtom cannot be resolved or if a circular dependency is detected.

The reason this function is a member of the IndirectObject is because resolving RefAtoms requires access to the ObjectSoup. The ObjectSoup is taken from the IndirectObject.

## Example

None.

