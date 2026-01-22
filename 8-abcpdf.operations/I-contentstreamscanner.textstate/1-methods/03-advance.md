# Advance Function

Advances the text position by an amount - typically the width of a glyph.

## Syntax

[C#]

```csharp
virtual double Advance(double delta, bool vertical)
```

[Visual Basic]

```vb
Overridable Function Advance(delta As double, vertical As bool) As Double
```

## Params

| **Name** | **Description** |
| --- | --- |
| delta | The amount to advance in unscaled text units. |
| vertical | Whether the advance should be horizontal or vertical. |
| return | The distance that the Text Matrix has been transformed by. |

## Notes

Advances the text position by an amount - typically the width of a glyph.

## Example

None
