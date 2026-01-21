---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | Validation Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Validation class. This is the base pure abstract class that stores and reports the validation status of Elements that are being validated. For custom validation reports you may derive from this class and implement any abstract methods. However generally you will want to derive from ValidationBase as it includes a number of useful housekeeping routines. ``` System.Object WebSupergoo.ABCpdf13.Elements.Validation WebSupergoo.ABCpdf13.Elements.ValidationBase ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| Validation | Initializes a new instance of the Validation class. | 
| Start | Called at the point each Element starts validation. | 
| Finish | Called at the point each Element finishes validation. | 
| Seen | Called to indicate that a particular RefAtom has been seen. | 
| ReportEntryVersion | Called to report the entry version. | 
| ReportUnknownEntryName | Called to report an entry with an unrecognized name. | 
| ReportIncorrectEntryValue | Called to report an entry with an incorrect value. | 
| ReportMissingRequiredEntry | Called to report a missing required entry. | 
| ReportNotIndirectObject | Called to report an object which should be indirect but is not. | 
| ReportIncorrectItemType | Called to report an object which is of the wrong type. | 
| ReportIncorrectNumberOfEntries | Called to report an array with an incorrect number of entries. | 
| ReportException | Called to report an Exception that was thrown during validation. | 
| ReportRecursiveStructure | Called to report detection of a recursive structure. | 

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