---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | AtomicArrayElement Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Class AtomicArrayElement. This class represents an array of atomic elements. By atomic, we mean elements that can be directly represented using a .NET equivalent such as a string or int. On the PDF side the elements that are acceptable may be types such as StringAtom or NameAtom. The set of acceptable types may be indicated using the AtomicTypes property. Since it is an array, the core Atom this class is created from should be an ArrayAtom. ``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.AtomicArrayElement ``` `Implements: IList, IList` `Type T : Can be string, int, double, double? or bool.` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| AtomicArrayElement | Create a new AtomicArrayElement. | 
| IndexOf | Determines the first index matching a specific value. | 
| Insert | Inserts an item into the array at the specified position. | 
| RemoveAt | Removes the item at the specified index. | 
| Add | Add an item to the end of the array. | 
| Clear | Removes all items from the array. | 
| Contains | Determines whether the array contains a specific value. | 
| CopyTo | Copies the items into an array. | 
| Remove | Removes the first matching value from the array. | 
| GetEnumerator | Returns an enumerator that iterates through the collection. | 
|  | inherited methods... | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Property | Description | 
| --- | --- |
| AtomicTypes | The Type of elements within the Array. | 
| Item[int index] | Gets or sets the items at the specified index. | 
| Count | Gets the number of items contained in the array. | 
|  | inherited properties... | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
        <tr> 
          <td>&nbsp; </td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
</table>