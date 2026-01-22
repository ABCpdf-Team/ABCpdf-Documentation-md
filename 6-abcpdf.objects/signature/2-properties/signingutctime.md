# SigningUtcTime Property

## Notes

The time of signing in UTC format.

When you call the Sign function, the UTC time is automatically updated.

Note that this property can only be relied on if the certificate is valid. You can check whether the certificate is valid using the Validate function.

You will not need to change the value of this property unless you are writing low level signature manipulation code.

If the format of the date in the PDF is incorrect, then querying the value of this property may result in an exception being thrown.

## Example

None.

