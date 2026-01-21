---
title: "04-item(intindex)"
css: "abcpdf-docs.css"
---

|  |  | Item(int index) Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp T ``` [Visual Basic] `T` | null | No | Gets or sets the Element at the specified index. | 

`ArgumentOutOfRangeException: Thrown if the index provided is not valid. NullReferenceException: Thrown if an attempt is made to assign a null value in a non-Nullable array.`

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
      
| Gets or sets the Element at the specified index. In C# this property is the indexer for the class. The Item property is used to access Elements within the Array. The ArrayAtom is accessed and used to create an Element of type T. In the case that T has multiple sub-types, default factories will result in an item of the correct subtype being created. The precise factory that should be used is determined at the point the ArrayElement is assigned to a property of another Element. So since different properties may use different factories, you should not share one ArrayElement between more than one property. Most ArrayElements cannot hold null values in a meaningful way. So in general, if you provide a null value this will result in an exception being raised. Occasionally it is appropriate for ArrayElements to hold null values represented as NullAtoms. You can indicate this is acceptable, by setting the Nullable property. |  |  | 
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