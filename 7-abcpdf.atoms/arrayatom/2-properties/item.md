# Item Property

| **Type** | **Default** | **Read Only** | **Description** |
| --- | --- | --- | --- |
|  | n/a | No | Get or set the Atom at the specified index. |

## Notes

Gets or sets the Atom at the specified index. In C# this property is the indexer for the class.

You can access an Atom directly or you can use one of the overloaded operators to specify numbers or strings. Using the overloads to access numbers or strings is more efficient than accessing an Atom and extracting the value from it.

You specify one of the overloads using the def parameter. If you are setting a value then this parameter is ignored. If you are getting a value then this parameter becomes the default value to be used if the underlying Atom was not the correct type. For example the default would be returned if you attempted to get an integer but the underlying Atom was actually a [StringAtom](stringatom/default.md).

The integer and double overload allow access to NumAtoms. The string overload allows access to StringAtom values while the Enum overload allows access to NameAtom values. Any Enum may be used and if the entry is not valid or available the string value of the Enum will be returned. The byte[] overload allows access to the raw data of the atom.

Atoms can exist in only one place at a time. If the Atom supplied is already contained by another object then a [Clone](1-atom/1-methods/1-clone.md) of the Atom is added.

Adding a null value will result in a [NullAtom](nullatom/default.md) being added to the array.

If the index is not a valid index this property throws an ArgumentOutOfRangeException.

## Example

None
