# SMask Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp PixMap ``` [Visual Basic] `PixMap` | n/a | No | Any soft image mask associated with this image | 

## Notes

Soft masks are higher quality than one bit masks but are less compatible with older viewing software, printer RIPs and formats like PDF/A.

If both a SMask and [Mask](mask.md) entry are specified, then the SMask will take priority.

## Example

None.