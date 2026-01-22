# Clone Function

## Syntax

[C#] IndirectObject Clone() [Visual Basic] Function Clone() As IndirectObject

## Params

## Notes

This function creates a new object that is a copy of this instance.

The copy is a deep copy and all contained objects are copied as part of the clone process. The copy is not associated with any ObjectSoup.

Note that many methods require that an object be part of a soup. For this reason it is quite common to call doc.ObjectSoup.Add with the newly cloned object before calling methods on it. If at a later date the object needs to be deleted this can be done using ObjectSoup.Remove.

## Example

None.

