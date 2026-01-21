---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | ObjectSoup Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A non-traditional collection of Indirect Objects making up the content of a PDF. This collection has some of the characteristics of an Array and some of a Dictionary. Objects are referred to by index - starting at zero - like an Array. However they do not move within the list because they are identified by index - like a Dictionary with numeric keys. We call this type of hybrid object a Soup. We assign it traditional interfaces to make it easier to use. ``` System.Object WebSupergoo.ABCpdf13.Objects.ObjectSoup ``` `Implements: IList, ICollection, IEnumerable, IList, ICollection, IEnumerable, IDisposable` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| Dispose | Dispose of the object. | 
| CopyTo | Copies the objects in the Soup to an Array. | 
| Add | Adds an object to the Soup. | 
| Clear | Removes all objects from the Soup. | 
| Contains | Determines whether the Soup contains a specific object. | 
| IndexOf | Determines the index of a specific object. | 
| Insert | Inserts an object into the Soup at the specified position. | 
| Remove | Removes an object from the Soup. | 
| RemoveAt | Removes an object at a specified position from the Soup. | 
| GetEnumerator | Gets an enumerator for the Soup. | 

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
| Count | The number of items in the Soup. | 
| Item | Gets or sets the object at the specified index. | 
| Catalog | The Catalog for the document. | 
| Convert | A Converter for the document. | 
| Trailer | The Trailer or XRef for the document. | 
| Revisions | The number of incremental updates. | 
| RevisionEOFs | This provides the end of trailer offsets within the underlying PDF stream. | 

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