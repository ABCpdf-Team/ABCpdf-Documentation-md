# TimestampHashAlgorithm Property

## Notes

This property enables you to specify the hash algorithm to be used for timestamp requests using your desired Time Stamping Authority (TSA).

In signature workflows there may be a number of different timestamps:

For convenience when a signature is created with SignatureCompliance set to a level above PAdES_B_B this value is used to compute the digests for all required timestamping operations.

Note that MD5 or SHA1 should not be used where PAdES conformance is required.

It is unlikely that you would need to change this from the default Oid for SHA256.

## Example

None.

