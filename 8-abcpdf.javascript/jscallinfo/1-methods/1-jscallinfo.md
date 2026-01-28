# JSCallInfo Constructor

Creates a new JavaScript call information object.

## Syntax

[C#]

```csharp
JSCallInfo(JSContext context, JSValue callee, bool isConstructCall, IList&lt;JSValue&gt; args)
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
