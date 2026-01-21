# CertificateCollection Constructor

CertificateCollection Constructor.

## Syntax

**[C#]**

```csharp
CertificateCollection()
CertificateCollection(Signature.CertificateCollection certs)
CertificateCollection(X509Certificate2 cert)
CertificateCollection(X509Certificate2[] certs)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub New
Sub New(certs As Signature.CertificateCollection)
Sub New(cert As X509Certificate2)
Sub New(certs() As X509Certificate2)
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| certs | A Signature.CertificateCollection object or an array of System.Security.Cryptography.X509Certificates.X509Certificate2 objects. | 
| cert | A System.Security.Cryptography.X509Certificates.X509Certificate2 object. | 

## Notes

These methods construct a Signature.CertificateCollection object. Signature.CertificateCollection does not store duplicate certificates, so only one certificate object among each set of duplicates is included if an array of X509Certificate2 is provided.

## Example

None.