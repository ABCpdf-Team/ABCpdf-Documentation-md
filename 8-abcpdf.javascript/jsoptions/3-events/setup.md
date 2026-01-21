# SetUp Event

Occurs after the JavaScript engine is initialized and before the specified JavaScript code is executed.

## Syntax

**[C#]**

```csharp
event Func SetUp;
```

<span class=language>[Visual Basic]</span>  
`Event SetUp As Func(Of JSCallInfo, Object)`
## Params

| Name | Description | 
| --- | --- |
| arg | A JSCallInfo providing only the context in JSCallInfo.Context. | 
| return | The return value is ignored. | 

## Notes

This event allows the set-up of the JavaScript environment. No JavaScript function is created for the delegate of the event.

## Example

Here, we implement the Field.display property.

[C#]

```csharp
using (Doc doc = new Doc()) {
  doc.Read(Server.MapPath("../mypics/sample.pdf"));
  JSOptions options = new JSOptions();
  options.SetUp += delegate (JSCallInfo arg) {
    JSValue prototype = arg.Context.GetFieldPrototype();
    if(!prototype.HasProperty("display")) {
      JSAccessorDescriptor desc = new JSAccessorDescriptor();
      desc.Configurable = false;
      desc.Enumerable = true;
      desc.Get = delegate (JSCallInfo info) {
        JSContext context = info.Context;
        int id = info.This.GetDocObjectID();
        if(id==0)
          return null;
        Annotation annot = (Annotation)context.Doc.ObjectSoup[id];
        Annotation.AnnotationFlags flags = annot.Flags;
        if((flags & Annotation.AnnotationFlags.Hidden)!=0)
          return 1;  // display.hidden
        int v = 0;  // display.visible
        if((flags & Annotation.AnnotationFlags.Print)==0)
          v |= 2; // display.noPrint
        if((flags & Annotation.AnnotationFlags.NoView)!=0)
          v = v ^ 2 | 1;  // display.hidden, display.noView
        return v;
      };
      desc.Set = delegate (JSCallInfo info) {
        if(info.ArgCount<2)
          return null;
        JSContext context = info.Context;
        int id = info.This.GetDocObjectID();
        if(id==0)
          return null;
        Annotation annot = (Annotation)context.Doc.ObjectSoup[id];
        Annotation.AnnotationFlags flags = annot.Flags;
        int v = info.Args[1].GetValueInt();
        switch(v) {
        case 0:  // display.visible
          flags = flags & ~Annotation.AnnotationFlags.Hidden
            & ~Annotation.AnnotationFlags.NoView
            | Annotation.AnnotationFlags.Print;
          break;
        case 1:  // display.hidden
          flags = flags & ~Annotation.AnnotationFlags.NoView
            | Annotation.AnnotationFlags.Print
            | Annotation.AnnotationFlags.Hidden;
          break;
        case 2:  // display.noPrint
          flags = flags & ~Annotation.AnnotationFlags.Hidden
            & ~Annotation.AnnotationFlags.NoView
            & ~Annotation.AnnotationFlags.Print;
          break;
        case 3:  // display.noView
          flags = flags & ~Annotation.AnnotationFlags.Hidden
            | Annotation.AnnotationFlags.Print
            | Annotation.AnnotationFlags.NoView;
          break;
        default: return null;
        }
        annot.Flags = flags;
        return null;
      };
      prototype.DefineProperty("display", desc);
    }
    return null;
  };
  options.LoadGlobals = true;
  doc.Form.RunJS("var f = this.getField(\"Text1\"); f.display = display.hidden;", options);
  doc.Save(Server.MapPath("hiddenfield.pdf"));
}
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc()
  doc.Read(Server.MapPath("../mypics/sample.pdf"))
  Dim field As Field = doc.Form("CheckBox1")
  Dim options As New JSOptions()
  AddHandler options.SetUp, Function(arg As JSCallInfo)
    Dim prototype As JSValue = arg.Context.GetFieldPrototype()
    If Not prototype.HasProperty("display") Then
      Dim desc As New JSAccessorDescriptor()
      desc.Configurable = False
      desc.Enumerable = True
      desc.Get = Function(info As JSCallInfo)
        Dim context As JSContext = info.Context
        Dim id As Integer = info.This.GetDocObjectID()
        If id = 0 Then
          Return Nothing
        End If
        Dim annot As Annotation = CType(context.Doc.ObjectSoup(id), Annotation)
        Dim flags As Annotation.AnnotationFlags = annot.Flags
        If (flags And Annotation.AnnotationFlags.Hidden) <> 0 Then
          Return 1 ' display.hidden
        End If
        Dim v As Integer = 0 ' display.visible
        If (flags And Annotation.AnnotationFlags.Print) = 0 Then
          v = v Or 2 ' display.noPrint
        End If
        If (flags And Annotation.AnnotationFlags.NoView) <> 0 Then
          v = v Xor 2 Or 1 ' display.hidden, display.noView
        End If
        Return v
      End Function
      desc.Set = Function(info As JSCallInfo)
        If info.ArgCount < 2 Then
          Return Nothing
        End If
        Dim context As JSContext = info.Context
        Dim id As Integer = info.This.GetDocObjectID()
        If id = 0 Then
          Return Nothing
        End If
        Dim annot As Annotation = CType(context.Doc.ObjectSoup(id), Annotation)
        Dim flags As Annotation.AnnotationFlags = annot.Flags
        Dim v As Integer = info.Args(1).GetValueInt()
        Select Case v
        Case 0 ' display.visible
          flags = flags And Not Annotation.AnnotationFlags.Hidden _
            And Not Annotation.AnnotationFlags.NoView _
            Or Annotation.AnnotationFlags.Print
        Case 1 ' display.hidden
          flags = flags And Not Annotation.AnnotationFlags.NoView _
            Or Annotation.AnnotationFlags.Print _
            Or Annotation.AnnotationFlags.Hidden
        Case 2 ' display.noPrint
          flags = flags And Not Annotation.AnnotationFlags.Hidden _
            And Not Annotation.AnnotationFlags.NoView _
            And Not Annotation.AnnotationFlags.Print
        Case 3 ' display.noView
          flags = flags And Not Annotation.AnnotationFlags.Hidden _
            Or Annotation.AnnotationFlags.Print _
            Or Annotation.AnnotationFlags.NoView
        Case Else
          Return Nothing
        End Select
        annot.Flags = flags
        Return Nothing
      End Function
      prototype.DefineProperty("display", desc)
    End If
    Return Nothing
  End Function
  options.LoadGlobals = True
  doc.Form.RunJS("var f = this.getField(""Text1""); f.display = display.hidden;", options)
  doc.Save(Server.MapPath("hiddenfield.pdf"))
End Using
```