---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | ContentStreamScanner Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A class to scan through a content stream keeping track of state while it does so. Subclass to collect or extract content as it is being scanned. ``` System.Object WebSupergoo.ABCpdf13.Operations.ContentStreamScanner ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| ContentStreamScanner | Create a new ContentStreamScanner. | 
| Call | Call the scanner using an owner and a content stream array. | 
| Process | Process a content stream keeping track of state. | 
| ProcessItem | Process an item in a content stream and update the graphics or text state to reflect the action of the item. | 
| ShowText | Show an item of text. | 
| Abort | Abort the current processing. | 

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
| Resources | A class for accessing reseources in the document. | 
| Operators | The set of operators which should be processed. | 
| DoShowText | Whether to call into the ShowText function. | 
| DoUnicode | Whether to convert text to Unicode or not. | 
| DoWidths | Whether to calcuate text widths or not. | 
| Warnings | Content streams contain operators and parameters. | 
| Stack | The current graphics stack. | 
| State | The current graphics state. | 
| Text | The current text state. | 

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