---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | TextOperation Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Operation to analyse and manipulate the text in a set of pages. ``` System.Object WebSupergoo.ABCpdf13.Operations.TextOperation ``` |  |  | 

</TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Method | Description | 
| --- | --- |
| TextOperation | TextOperation Constructor. | 
| GetText | Get all the text in the page contents. | 
| Select | Select a range of text in the document. | 
| Group | Group a range of text fragments into a set of lines. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD vAlign=top>&nbsp;</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Property | Description | 
| --- | --- |
| ClippedTextTolerance | How much overlap to require clipped text to have before it is defined as visible. | 
| Direction | The default direction for text. | 
| Hyphenation | Whether to de-hyphenate words that appear to be split across two lines. | 
| NativeColors | Whether to provide native colors such as CMYK, separations and spot colors, or whether to convert all colors to RGB. | 
| PageContents | The pages to be operated upon. | 
| ShowArtifactText | Whether to show text content that is marked as an artifact. | 
| ShowClippedText | Whether to show text which is invisible because it is affected by a clip path. | 
| ShowObscuredText | Whether to show overlapping repeated text content. | 
| Substitutions | A set of character to string substitutions used for translating typographic characters like ligatures into more normal text. | 
| TabAffinity | The minimum distance at which two text fragments will be assumed to be part of separate tab groups. | 
| TabChar | The character used to separate out tab groups when GetText is called. | 
| TextObjects | Whether to get information on the BT and ET text object markers used to contain and group text operators. | 
| WordAffinity | The minimum distance at which two fragments will be assumed to be part of one undivided word. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR>
        <TR>
          <TD>&nbsp; </TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>