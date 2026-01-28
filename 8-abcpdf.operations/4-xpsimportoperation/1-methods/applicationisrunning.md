# ApplicationIsRunning Function

Gets a value indicating whether an import application is
            running for this XpsImportOperation.

## Syntax

[C#]

```csharp
bool ApplicationIsRunning(ImportApplicationType app)
```

## Params

| **Name** | **Description** |
| --- | --- |
| app | The import application. |
| return | Whether the application is running. |

## Notes

This function indicates whether an application is running for this XpsImportOperation when the process reuse for the application is enabled with [EnableApplicationReuse](enableapplicationreuse.md).

## Example

None
