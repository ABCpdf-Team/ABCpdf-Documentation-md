---
title: "02-item(intindex)"
css: "abcpdf-docs.css"
---

|  |  | Item(int index) Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp T ``` [Visual Basic] `T` | null | No | Gets or sets the items at the specified index. | 

`ArgumentOutOfRangeException: Thrown if the index provided is not valid.`

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Gets or sets the items at the specified index. In C# this property is the indexer for the class. The Item property is used to access items within the Array. The ArrayAtom is accessed and used to create a value of type T. If the type indicated is string then a null string will be interpreted as an empty string. If the type indicated is a double? then a null value will be interpreted as a NullAtom. All other types are non-nullable. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>