# UseActiveX Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to enable ActiveX. | 

## Notes

This property determines whether ActiveX is enabled.

By default ActiveX is disabled when rendering HTML documents.

This is done for good security reasons and we strongly recommend that you do not change this setting.

However if you are sure that your source documents do not pose a security risk you can enable ActiveX using this setting.

Compatibility. Not all ActiveX controls are compatible with ABCpdf. In particular some rely on being able to draw direct to screen which stops ABCpdf being able to use them.

## Example

None.