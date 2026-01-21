---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | TextFragment Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A fragment of text as it appears in a document. Each TextFragment spans a part of a PDF stream drawing operator. The part may be the entire of the text drawn by the operator or it may be a section of the text within that operator. For example the PDF text drawing operator "(Once upon a time) Tj" draws that text. If you search for the word "upon" the TextFragment which is returned will reference the complete operator via the StreamOffset and StreamLength properties but properties like the Text and Rect will span only the word "upon" within that operator. ``` System.Object WebSupergoo.ABCpdf13.Operations.TextFragment ``` |  |  | 

</TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Method | Description | 
| --- | --- |
| Focus | Prepare document for drawing at the fragment location. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD vAlign=top>&nbsp;</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Property | Description | 
| --- | --- |
| Font | The font object used for drawing this text fragment. | 
| FontColor | The color used for drawing this text fragment. | 
| FontColorSpace | The ColorSpace used for drawing this text fragment. | 
| FontSize | The effective font size used for drawing this text fragment. | 
| FontObliqueAngle | The skew angle of the font as used for oblique styles to simulate italic. | 
| RenderingMode | The text rendering mode used for drawing this text fragment. | 
| PageID | The ID of the Page on which this text fragment is located. | 
| StreamID | The Stream ID of the content stream in which this text fragment is located. | 
| StreamOffset | The offset within the content stream to the start of the drawing operation that contains this fragment. | 
| StreamLength | The length within the content stream of the drawing operation that contains this fragment. | 
| TextOffset | The offset to the the Text of this fragment. | 
| TextSpanIndex | The zero based index of the drawing operator text array item that contains this fragment. For non text array operators this value is zero. | 
| Rect | The rectangle that contains the text of the fragment. | 
| Rotation | The angle of rotation of the fragment in degrees. | 
| Text | The text of the fragment. A fragment may span only a portion of the complete text drawing operator. | 
| RawText | The text specified in the drawing operator or the text array item of the drawing operator. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR>
        <TR>
          <TD>&nbsp; </TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>