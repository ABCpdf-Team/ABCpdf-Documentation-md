---
title: "startpool"
css: "abcpdf-docs.css"
---

# StartPool Method

Start the process pool for the HTML Engine.

## Syntax

**[C#]**

```csharp
bool StartPool()
```

**[Visual Basic]**

`Function StartPool() As Boolean`
## Params

| Name | Description | 
| --- | --- |
| return | Whether the process pool is started anew. | 

## Notes

This starts the process pool for the HTML Engine (without rendering an HTML page).

This method returns false if the process pool has been started before the method is called.

## Example

None.