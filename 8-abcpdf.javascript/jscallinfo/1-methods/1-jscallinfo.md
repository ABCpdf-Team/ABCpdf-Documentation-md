# JSCallInfo Constructor

Creates a new JavaScript call information object.

## Syntax

[C#]

```csharp
JSCallInfo(JSContext context, JSValue callee, bool isConstructCall, IList&lt;JSValue&gt; args)
```

[Visual Basic]

```vb
Sub New(context As JSContext, callee As JSValue, isConstructCall As Boolean, args As IList(Of JSValue))
```

## Params

| **Name** | **Description** |
| --- | --- |
| context | The JavaScript context. This must be non-null/non-Nothing. |
| callee | The callee. |
| isConstructCall | Indicates whether the call is a 'new' call. |
| args | The arguments to the call. |

## Notes

The constructor creates a new JavaScript call information object.

## Example

None
