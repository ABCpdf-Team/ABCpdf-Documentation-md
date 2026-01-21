# VetText Function

Make a string of text safe for use in a specified encoding.

## Syntax

**[C#]**

```csharp
string VetText(LanguageType type, bool vertical, string text)
string VetText(LanguageType type, bool vertical, string text, Func substitute)
```

<span class=language>[Visual
            Basic]</span>  

```
Function VetText(type As LanguageType, vertical As Bool, text As String) As String
Function VetText(type As LanguageType, vertical As Bool, text As String, substitute as Func) As String
```

</p>`may throw Exception()` ## Params | Name | Description | | --- | --- | | type | The language type for the desired encoding. | | vertical | Whether the writing direction should be horizontal or vertical. | | text | The text to vet. | | substitute | A function taking a character and returning a substitute character. | | return | The vetted text. | ## Notes Make a string of text safe for use in a specified encoding.

Any characters which are not present in the encoding will be substituted with ones that are.

You can optionally specify a function to do the character substitution.

If your substitution function returns a character which is not present in the encoding an exception will be raised.

## Example

None.