# SkipEngineDependencyCheck Method

## Syntax

[C#] void SkipEngineDependencyCheck()

## Params

## Notes

This skips the check of engine-dependent options to avoid an exception. The values of engine-dependent options should be set after Engine has been set because the value applies only to the selected engine. To make sure that the set engine-dependent options is applied to the engine that is used for HTML import or process pool operation (e.g. StartPool), the HTML import or process pool operation checks for the equality of the set values and the values for the newly specified engine.

MaxProcesses depends on the selected engine.

## Example

None.

