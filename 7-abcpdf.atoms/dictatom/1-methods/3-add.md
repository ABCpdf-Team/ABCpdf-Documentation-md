---
title: "3-add"
css: "abcpdf-docs.css"
---

|  |  | Add Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add an item to the dictionary. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void Add(string key, Atom atm) void Add(string key, int num) void Add(string key, double real) void Add(string key, string str) ``` [Visual Basic] ``` Sub Add(key As String, atm As Atom) Sub Add(key As String, num As Integer) Sub Add(key As String, real As Double) Sub Add(key As String, str As String) ``` `may throw ArgumentException()` `may throw ArgumentNullException()` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| key | The string to use as the key of the element to add. | 
| atm | The Atom to be added. | 
| num | The integer to be added. | 
| real | The floating point value to be added. | 
| str | The string to be added. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This method adds an item to the dictionary. You can add an Atom directly into the dictionary or you can use one of the overloaded operators to add numbers or strings. When you add a string this is encapsulated within a StringAtom and then inserted. When you add an integer or floating point value this is converted to a NumAtom and then inserted. These operations are more efficient than creating an Atom and adding it yourself. Atoms can exist in only one place at a time. If the Atom supplied is already contained by another object then a Clone of the Atom is added. Adding a null value will result in a NullAtom being added to the dictionary. If the key is null then this method will throw an ArgumentNullException. If the key is already present in the dictionary then this method will throw an ArgumentException. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>