# ReusesApplication Function

Gets a value indicating whether an import application process is
            to be kept running and reused.

## Syntax

[C#]

```csharp
bool ReusesApplication(ApplicationType app)
```

[Visual Basic]

```vb
Function ReusesApplication(app As ImportApplicationType) As Boolean
```

## Params

| **Name** | **Description** |
| --- | --- |
| app | The import application. |
| return | Whether the application process is to be kept running and reused. |

## Notes

This function returns the reuse status of an application.

The reuse status can be changed with [EnableApplicationReuse](enableapplicationreuse.md).

## Example

None
