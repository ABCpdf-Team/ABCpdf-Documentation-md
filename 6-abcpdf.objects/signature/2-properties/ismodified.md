# IsModified Property

## Example

This property allows you to determine if the PDF has been tampered with after signing.

It is important to understand that certain types of updates are allowed. The validity of this property relates to the validity of the particular revision of the document. So it allows you to determine if the original PDF has been tampered with in any way.

However it is possible to update PDF by incrementally updating the revision. This will provide a document which contains modifications but can be backtracked to show the exact state of the document at the point that a particular signature was applied.

Most commonly this is needed when multiple signatures are being applied as each signature needs to be applied to a new revision of the document and to be valid for that particular revision.

See also the Validate function.

