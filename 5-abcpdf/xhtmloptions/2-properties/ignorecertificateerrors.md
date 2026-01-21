---
title: "ignorecertificateerrors"
css: "abcpdf-docs.css"
---

# IgnoreCertificateErrors Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to ignore certificate-related errors. | 

## Notes

This property determines whether certificate-related errors are ignored or not.

When retrieving pages via https URLs, ABCpdf will check that the SSL certificate is valid and trusted. If it is not you may not wish to proceed with the HTML render and instead throw an exception.

Using this property you can control whether error will be ignored or reported.

## Example