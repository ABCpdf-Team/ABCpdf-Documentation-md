# ValidationInfo Class

The validation properties of a PDF signature.

``` System.Object WebSupergoo.ABCpdf13.Objects.Signature.ValidationInfo ```

## Method Description &nbsp;

## Property Description SignerName The name of the signer of the signature as specified on the signer's certificate. SigningTime The most authoritative UTC signing time for the signature. SigningTimeIsTrusted Whether the SigningTime is an embedded timestamp. RevocationCheckingTime "The time the signature was validated. SignatureIsLTVEnabled Whether the signature has long-term validation information. DocumentRevision The document revision the signature applies to. SigningCertificate The X509 certificate used to sign the PKCS#7 signature. CertificateChain The X509Chain as used to validate the signature.