# DSSPolicy Property

## Notes

The RevocationPolicy enumeration may take the following values:

With the OcspThenCrl and CrlThenOcsp selectors, the first method is used and the responses checked. If they are all valid then the process will go no further and the responses will be embedded in the DSS. If the responses are unavailable or invalid then the second method will be tried instead.

## Example

None.

