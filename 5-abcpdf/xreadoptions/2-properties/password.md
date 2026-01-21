---
title: "password"
css: "abcpdf-docs.css"
---

# Password Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp string ``` [Visual Basic]`String` | null | No | Gets or sets the password needed to read the source. | 

## Notes

Specify with this property the password for accessing the source, for example, when [read](../../doc/1-methods/read.md)ing a PDF document.

It is used for importing MS Word or MS Excel documents when using Microsoft Office via the XpsAny and MSOffice ReadModule. Note that for other Office applications, eg. MS PowerPoint, ABCpdf cannot import password protected documents. Currently, certain features such as form fields conversion may be disabled if the document is password protected, even if the correct password is supplied.

## Example

None.