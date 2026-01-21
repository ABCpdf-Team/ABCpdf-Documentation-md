---
title: "03-item(stringkey)"
css: "abcpdf-docs.css"
---

|  |  | Item(string key) Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp T ``` [Visual Basic] `T` | null | No | Gets or sets the Element at the specified index. | 

`KeyNotFoundException: Thrown if getting an item, but the specified key was not found. NullReferenceException: Thrown if an attempt is made to assign a null value.`

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
      
| Gets or sets the Element at the specified index. In C# this property is the indexer for the class. The Item property is used to access Elements within the dictionary. The DictAtom is accessed and used to create an Element of type T. In the case that T has multiple sub-types, default factories will result in an item of the correct subtype being created. The precise factory that should be used is determined at the point the DictElement is assigned to a property of another Element. So since different properties may use different factories, you should not share one DictElement between more than one property. DictElements cannot hold null values in a meaningful way. So if you provide a null value, this will result in an exception being raised. If the specified key is not found, a get operation throws a KeyNotFoundException, and a set operation creates a new element with the specified key. |  |  | 
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