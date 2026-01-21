---
title: "1-processingobject"
css: "abcpdf-docs.css"
---

# ProcessingObject Event

Occurs just before an IndirectObject is processed.

## Syntax

**[C#]**

```csharp
event ProcessingObjectEventHandler ProcessingObject;

delegate void ProcessingObjectEventHandler(object sender, ProcessingObjectEventArgs e);
```

<span class=language>[Visual Basic]</span>  

```
Event ProcessingObject As ProcessingObjectEventHandler

Delegate Sub ProcessingObjectEventHandler(sender As Object, e As ProcessingObjectEventArgs);
```

## Params

| Name | Description | 
| --- | --- |
| sender | The Operation firing the event. | 
| e | The ProcessingObjectEventArgs used to control the operation. | 

## Notes

Typically you handle the ProcessingObject event in order to determine properties about an [IndirectObject](../../../6-abcpdf.objects/1-indirectobject/default.md) before processing.

Because the handler passes an EventArgs class which inherits from CancelEventArgs you can also choose to cancel the operation on the IndirectObject.

To associate the event with your event handle add an instance of the ProcessingObjectEventHandler delegate to the event. The event handler will be called whenever the event occurs.

## Example

See the [RecolorOperation.Recolor](../../3-recoloroperation/1-methods/recolor.md) method.