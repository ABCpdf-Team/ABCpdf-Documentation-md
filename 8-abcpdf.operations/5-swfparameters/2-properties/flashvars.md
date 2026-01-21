---
title: "flashvars"
css: "abcpdf-docs.css"
---

|  |  | FlashVars Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp IEnumerable> ``` [Visual Basic]`IEnumerable(Of KeyValuePair(Of String, Object))` | null | No | The Flash variables. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property specifies the Flash variables. The object values can be any of the following: SwfActionValue.Undefined – the undefined value. SwfActionValue.Null – the null value. A Boolean – a primitive Boolean. A Char – a primitive string consisting of one character. A SByte, Byte, Int16, UInt16, or Int32 – a primitive number (32-bit integer). A UInt32, Int64, or UInt64 – a primitive number (32-bit integer if it is within the range of 32-bit integer; double-precision floating-point number, otherwise). A Single – a primitive number (single-precision floating-point number). A Double – a primitive number (double-precision floating-point number). A Decimal – a primitive number (32-bit integer if it is an integer within the range of 32-bit integer; double-precision floating-point number, otherwise). A String – a primitive string. IEnumerable> – an object with KeyValuePair.Key as the property names and KeyValuePair.Value after this conversion as the property values. IEnumerable – an array with the objects after this conversion as the element values. Reference semantics of objects is supported. When the same IEnumerable> or the same IEnumerable is in different parts of this property value, the same object is used. In particular, you can create objects and properties/element values that form circular references. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here, we import the chart in the frame at two seconds into a Flash movie. **[C#]** ```csharp Doc doc = new Doc(); using(SwfImportOperation operation = new SwfImportOperation()) { operation.Doc = doc; operation.ContentAlign = ContentAlign.Top; operation.ContentScaleMode = ContentScaleMode.ShowAll; operation.ProcessingObject += delegate(object sender, ProcessingObjectEventArgs e) { if(e.Info.SourceType==ProcessingSourceType.MultiFrameImage && e.Info.FrameNumber.HasValue) e.Info.FrameNumber = 1+(long)(e.Info.FrameRate.Value*2); }; const int chartWidth = 400; const int chartHeight = 300; SwfParameters parameters = new SwfParameters(); parameters.StageWidth = chartWidth*20; parameters.StageHeight = chartHeight*20; Dictionary flashVars = new Dictionary(); flashVars.Add("chartWidth", chartWidth); flashVars.Add("chartHeight", chartHeight); flashVars.Add("dataXML", "" +"" +"" +"" +"" +""); parameters.FlashVars = flashVars; operation.Parameters = parameters; operation.Import(Server.MapPath("Column3D.swf")); } doc.Save(Server.MapPath("chart.pdf")); doc.Clear(); ``` [Visual Basic] ``` Dim theDoc As Doc = New Doc() Using theOperation As New SwfImportOperation theOperation.Doc = theDoc theOperation.ContentAlign = ContentAlign.Top theOperation.ContentScaleMode = ContentScaleMode.ShowAll AddHandler theOperation.ProcessingObject, AddressOf Processing Const theChartWidth As Integer = 400 Const theChartHeight As Integer = 300 Dim theParameters As SwfParameters = New SwfParameters() theParameters.StageWidth = theChartWidth * 20 theParameters.StageHeight = theChartHeight * 20 Dim theFlashVars As Dictionary(Of String, Object) = New Dictionary(Of String, Object)() theFlashVars.Add("chartWidth", theChartWidth) theFlashVars.Add("chartHeight", theChartHeight) theFlashVars.Add("dataXML", _ "" _ & "" _ & "" _ & "" _ & "" _ & "") theParameters.FlashVars = theFlashVars theOperation.Parameters = theParameters theOperation.Import(Server.MapPath("Column3D.swf")) End Using theDoc.Save(Server.MapPath("chart.pdf")) theDoc.Clear() Private Shared Sub Processing(sender As Object, e As ProcessingObjectEventArgs) If e.Info.SourceType = ProcessingSourceType.MultiFrameImage _ AndAlso e.Info.FrameNumber.HasValue Then e.Info.FrameNumber = 1 + CLng(e.Info.FrameRate.Value * 2) End If End Sub ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>