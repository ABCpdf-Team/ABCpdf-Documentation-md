# CustomSigner2 Property

## Notes

The delegate type called to perform custom signing and timestamping of the PDF.

The definition of the SigningDelegate2 delegate is as follows.

[C#] delegate byte[] SigningDelegate2(byte[] data, State state); [Visual Basic] Delegate Function SigningDelegate2(data As Byte(), state As State) As Byte();

Because a call to Sign can generate both signing and timestamping callbacks, the state parameter allows you to determine which is required. The State flags enum can hold the following values,

For signing...

The type of data passed to your delegate is determined by the data type you specify when you call the Sign method. The default type is DataType.Pkcs9Digest which is what will be used if you do not specify a type.

For DataType.Pkcs9Digest the data is an ASN.1 encoded PKCS9 digest of the PDF content which includes the digest of the document data with additional attributes required according to any desired CompliancePades level that you have specified. For DataType.RawDigest the data is the raw digest of the document data.

In either case ABCpdf will create the digest using the algorithm specified by the Oid passed to the Signature.Sign method. Where the Sign method overload does not take an Oid the default algorithm of SHA256 will be used.

For best results the CustomSigner should return the raw signature of this data such as that returned by RSACryptoServiceProvider.SignData (.NET 4) or RSACng.SignData (.NET 5+). This ensures that ABCpdf can add any additional unsigned attributes required for PAdES compliance. When using RSACng you should use RSASSA-PKCS1-v1.5 rather than RSASSA-PSS padding.

If ABCpdf detects that the data returned is already in PKCS7 CMS format it will embed that data into the document as is, with no further processing. This is sometimes needed to accommodate certain third-party signing solutions. In this case any desired compliance will be dependent upon your solution provider.

The best way to determine the type of data your signing provider returns, is to paste the byte array as a hexadecimal string into a decoder such as the LAPO ASN.1 JavaScript Decoder. If it can be decoded it is already in PKCS7 format. If it cannot then it is most likely the raw signature of the digest.

For timestamping...

If a TimestampServiceUrl is provided then this will be used for time stamping, but if one is not provided, then the custom signer will be used.

By default for timestamping you are provided an RFC 3161 time stamp request and you should return an RFC 3161 time stamp response.

However you can change the input and output timestamp data types by setting appropriate flags in the DataType parameter when calling Timestamp or Sign.

Also...

When writing code against your signing provider it is prudent to Validate the document to ensure you are providing correct data. See the example below for details.

## Example

The following example shows how an external delegate might be used.

[C#] X509Certificate2 cert = FindCertificate(); if (cert == null) return; // no certificate found using var doc = new Doc(); doc.Read(Server.MapPath("mypics/BlankSignature.pdf")); var sig = (Signature)doc.Form.Fields["Signature1"]; sig.CustomSigner2 = ExternalSigner; sig.Reason = "Test External Signing"; // Just use public certificate from file - i.e. do not obtain from registry var gs = new X509Certificate2(Server.MapPath("GlobalSign.cer")); sig.Sign(gs, true, new Oid(CryptoConfig.MapNameToOID("SHA512")), X509IncludeOption.EndCertOnly); // here we commit and validate to ensure the data is correct sig.Commit(); sig = (Signature)doc.Form.Fields["Signature1"]; // signature must be re-retrieved after a Commit/Save if (!sig.Validate()) throw new Exception("Signing failed!"); doc.Save(Server.MapPath("SignedDoc.pdf")); [Visual Basic] Dim cert As X509Certificate2 = FindCertificate() If cert = Nothing Then Return End If ' no certificate found Using doc As New Doc() doc.Read(Server.MapPath("mypics/BlankSignature.pdf")) Dim sig As Signature = DirectCast(doc.Form.Fields("Signature1"), Signature) sig.CustomSigner2 = ExternalSigner sig.Reason = "Test External Signing" ' Just use public certificate from file - i.e. do not obtain from registry Dim gs = New X509Certificate2(Server.MapPath("GlobalSign.cer")) sig.Sign(gs, True, New Oid(CryptoConfig.MapNameToOID("SHA512")), X509IncludeOption.EndCertOnly) ' here we commit and validate to ensure the data is correct sig.Commit() sig = DirectCast(doc.Form.Fields("Signature1"), Signature) ' signature must be re-retrieved after a Commit/Save If Not sig.Validate() Then Throw New Exception("Signing failed!") End If doc.Save(Server.MapPath("SignedDoc.pdf")) End Using

The code above uses the following External Signer.

[C#] byte[] ExternalSigner(byte[] data, Signature.State state) { var password = new SecureString(); // needs value var rsa = (RSACryptoServiceProvider)cert.PrivateKey; var cspParams = new CspParameters(1, rsa.CspKeyContainerInfo.ProviderName, rsa.CspKeyContainerInfo.UniqueKeyContainerName) { KeyPassword = password, Flags = CspProviderFlags.NoPrompt }; var service = new RSACryptoServiceProvider(cspParams); return service.SignData(data, CryptoConfig.MapNameToOID("SHA512")); } X509Certificate2 FindCertificate() { string serial = "10 20 30 10 40 10 40 50 60 10 20 30"; // needs value X509Certificate2 cert = null; var store = new X509Store(StoreName.My, StoreLocation.CurrentUser); try { store.Open(OpenFlags.ReadOnly | OpenFlags.OpenExistingOnly | OpenFlags.MaxAllowed); var certs = store.Certificates.Find(X509FindType.FindBySerialNumber, serial, false); if (certs.Count == 1) { cert = store.Certificates.Find(X509FindType.FindBySerialNumber, serial, false)[0]; if (cert.PrivateKey is RSACryptoServiceProvider == false) cert = null; } } finally { store.Close(); } return cert; } [Visual Basic] Private Function ExternalSigner(data As Byte(), state As Signature.State) As Byte() Dim password = New SecureString() ' needs value Dim rsa = DirectCast(cert.PrivateKey, RSACryptoServiceProvider) Dim cspParams = New CspParameters(1, rsa.CspKeyContainerInfo.ProviderName, rsa.CspKeyContainerInfo.UniqueKeyContainerName) With { _ Key .KeyPassword = password, _ Key .Flags = CspProviderFlags.NoPrompt _ } Dim service = New RSACryptoServiceProvider(cspParams) Return service.SignData(data, CryptoConfig.MapNameToOID("SHA512")) End Function Private Function FindCertificate() As X509Certificate2 Dim serial As String = "10 20 30 10 40 10 40 50 60 10 20 30" ' needs value Dim cert As X509Certificate2 = Nothing Dim store = New X509Store(StoreName.My, StoreLocation.CurrentUser) Try store.Open(OpenFlags.[ReadOnly] Or OpenFlags.OpenExistingOnly Or OpenFlags.MaxAllowed) Dim certs = store.Certificates.Find(X509FindType.FindBySerialNumber, serial, False) If certs.Count = 1 Then cert = store.Certificates.Find(X509FindType.FindBySerialNumber, serial, False)(0) If TypeOf cert.PrivateKey Is RSACryptoServiceProvider = False Then cert = Nothing End If End If Finally store.Close() End Try Return cert End Function

