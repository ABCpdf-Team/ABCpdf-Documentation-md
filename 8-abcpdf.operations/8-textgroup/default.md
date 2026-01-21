---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | TextGroup Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A group of text fragments that belong together. The essence of a TextFragment is that it spans only a small section of text. As such it may be necessary to group fragments together. For example take the following PDF drawing instruction sequence: `[ (There) 400 (was) 400 (Eru,) 300 (the One) ] TJ` This sequence wiill write out the text "There was Eru, the One". There are no space characters here and the spacing is indicated by character placement (the numbers) instead. Selecting the phrase "was Eru" will result in two TextFragments the first of which will correspond to "was" and the second to "Eru". The two TextFragment.Rect properties are not connected because there is a 400 wide gap between them. Also there is no space character so simply concatenating the text in the fragments would result in "wasEru". Using the TextOperation.Group method will group them into one TextGroup with the Text "was Eru" (space inserted) and a Rect corresponding to the complete selected phrase. ``` System.Object WebSupergoo.ABCpdf13.Operations.TextGroup ``` |  |  | 

</TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Method | Description | 
| --- | --- |
| none |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD vAlign=top>&nbsp;</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Property | Description | 
| --- | --- |
| PageID | The ID of the Page on which this group is located. | 
| Rect | The rectangle that contains the group. | 
| Text | The text of the group. | 
| TextFragments | The text fragments in the group. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR>
        <TR>
          <TD>&nbsp; </TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>