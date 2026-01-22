# SigningRevision Property

## Notes

The revision at which the signature was signed.

Content can be added to a document after signature. Most commonly this occurs if someone wishes to countersign an already signed document.

The original signature remains valid because it applies to the original document but you may wish to indicate that the document has been changed.

If the document has been modified in this way the SigningRevision will be less than the Doc.ObjectSoup.Revisions.

To detect the actual visible differences you would need to render the document at each revision using the XReadOptions.SkipRevisions property.

Note that you should check the IsModified property before relying on the value of this property.

## Example

None.

