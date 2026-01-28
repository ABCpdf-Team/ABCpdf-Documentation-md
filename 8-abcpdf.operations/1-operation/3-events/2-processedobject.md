# ProcessedObject Event

Occurs just after an IndirectObject has been processed.

## Syntax

[C#]

```csharp
event ProcessedObjectEventHandler ProcessedObject;delegate void ProcessedObjectEventHandler(object sender, <a href="../../2-processedobjecteventargs/default.htm">ProcessedObjectEventArgs</a> e); <!--notcode-->
```

## Params

| **Name** | **Description** |
| --- | --- |
| sender | The Operation firing the event. |
| e | The ProcessedObjectEventArgs used to report back the status of the operation. |

## Notes

Typically you handle the ProcessedObject event in order to post-process an [IndirectObject](6-abcpdf.objects/1-indirectobject/default.md).

To associate the event with your event handle add an instance of the ProcessedObjectEventHandler delegate to the event. The event handler will be called whenever the event occurs.

## Example

See the [RecolorOperation.Recolor](../../3-recoloroperation/1-methods/recolor.htm) method.
