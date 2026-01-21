---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | ProcessingInfo Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Provides generic information relating to the Operation.ProcessingObject event. The information about the source of the operation is available here when ProcessingObjectEventArgs.Object is null if the source is in a non-PDF format. ``` System.Object WebSupergoo.ABCpdf13.Operations.ProcessingInfo ``` |  |  | 

</TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Method | Description | 
| --- | --- |
| ProcessingInfo | ProcessingInfo Constructor. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Property | Description | 
| --- | --- |
| SourceType | Gets the type of the source object to be processed and the stage of operation. | 
| Handled | Gets or sets a value that indicates whether the event handler has handled the event so that the operation skips the default processing. | 
| X | Gets the x-coordinate of the location of the source object. | 
| Y | Gets the y-coordinate of the location of the source object. | 
| Width | Gets the width of the source object. | 
| Height | Gets the height of the source object. | 
| DocNumber | Gets or sets the document number of the source document being/to be processed. | 
| DocCount | Gets the number of documents in the source object. | 
| PageNumber | Gets or sets the page number of the source page being/to be processed. | 
| PageCount | Gets the number of pages in the source object. | 
| FrameNumber | Gets or sets the frame number of the source frame being/to be processed. | 
| FrameCount | Gets the number of frames in the source object. | 
| FrameRate | Gets the number of frames per second for the source object. | 
| BackgroundColor | Gets the background color of the source object. | 
| StreamPosition | Gets or Sets the stream position of the source object, if applicable. | 
| StreamLength | Gets the stream length of the source object, if applicable. | 
| Text | Gets the unicode Text of the Source Event, if applicable. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR>
        <TR>
          <TD>&nbsp; </TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>