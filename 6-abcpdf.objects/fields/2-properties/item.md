---
title: "item"
css: "abcpdf-docs.css"
---

|  |  | Item Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Field this[int index] ``` `Field this[string name]` [Visual Basic] `Default Property Item(index As Integer) As Field` `Default Property Item(name As String) As Field` | n/a | No | Get or set the item at the specified index. | 

`may throw ArgumentOutOfRangeException()` `may throw NotSupportedException()`

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Gets or sets the item at the specified location. In C# this property is the indexer for the class. The index specified may be a zero based numeric index. If the index is not a valid index this property throws an ArgumentOutOfRangeException. Alternatively it may be a string specifying a field name. If the name is not one which matches a Field in the collection then a null value will be returned. All Fields collections are read only so attempting to assign an item using this function will generate a NotSupportedException. |  |  | 
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