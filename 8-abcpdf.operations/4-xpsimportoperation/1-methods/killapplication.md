# KillApplication Function

Terminates a running import application.

## Syntax

[C#]

```csharp
bool KillApplication(ImportApplicationType app)
```

## Params

| **Name** | **Description** |
| --- | --- |
| app | The import application. |
| return | Whether the application has been running and killed. |

## Notes

This function terminates an application [ running](applicationisrunning.md) for this XpsImportOperation when the process reuse for the application is enabled with [EnableApplicationReuse](enableapplicationreuse.md).

## Example

None
