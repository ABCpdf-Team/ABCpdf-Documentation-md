---
title: "setup"
css: "abcpdf-docs.css"
---

|  |  | SetUp Event |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Occurs after the JavaScript engine is initialized and before the specified JavaScript code is executed. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp event Func SetUp; ``` [Visual Basic]`Event SetUp As Func(Of JSCallInfo, Object)` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| arg | A JSCallInfo providing only the context in JSCallInfo.Context. | 
| return | The return value is ignored. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This event allows the set-up of the JavaScript environment. No JavaScript function is created for the delegate of the event. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here, we implement the Field.display property. [C#] ```csharp using (Doc doc = new Doc()) { doc.Read(Server.MapPath("../mypics/sample.pdf")); JSOptions options = new JSOptions(); options.SetUp += delegate (JSCallInfo arg) { JSValue prototype = arg.Context.GetFieldPrototype(); if(!prototype.HasProperty("display")) { JSAccessorDescriptor desc = new JSAccessorDescriptor(); desc.Configurable = false; desc.Enumerable = true; desc.Get = delegate (JSCallInfo info) { JSContext context = info.Context; int id = info.This.GetDocObjectID(); if(id==0) return null; Annotation annot = (Annotation)context.Doc.ObjectSoup[id]; Annotation.AnnotationFlags flags = annot.Flags; if((flags & Annotation.AnnotationFlags.Hidden)!=0) return 1; // display.hidden int v = 0; // display.visible if((flags & Annotation.AnnotationFlags.Print)==0) v \|= 2; // display.noPrint if((flags & Annotation.AnnotationFlags.NoView)!=0) v = v ^ 2 \| 1; // display.hidden, display.noView return v; }; desc.Set = delegate (JSCallInfo info) { if(info.ArgCount[Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) Dim field As Field = doc.Form("CheckBox1") Dim options As New JSOptions() AddHandler options.SetUp, Function(arg As JSCallInfo) Dim prototype As JSValue = arg.Context.GetFieldPrototype() If Not prototype.HasProperty("display") Then Dim desc As New JSAccessorDescriptor() desc.Configurable = False desc.Enumerable = True desc.Get = Function(info As JSCallInfo) Dim context As JSContext = info.Context Dim id As Integer = info.This.GetDocObjectID() If id = 0 Then Return Nothing End If Dim annot As Annotation = CType(context.Doc.ObjectSoup(id), Annotation) Dim flags As Annotation.AnnotationFlags = annot.Flags If (flags And Annotation.AnnotationFlags.Hidden) <> 0 Then Return 1 ' display.hidden End If Dim v As Integer = 0 ' display.visible If (flags And Annotation.AnnotationFlags.Print) = 0 Then v = v Or 2 ' display.noPrint End If If (flags And Annotation.AnnotationFlags.NoView) <> 0 Then v = v Xor 2 Or 1 ' display.hidden, display.noView End If Return v End Function desc.Set = Function(info As JSCallInfo) If info.ArgCount |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>