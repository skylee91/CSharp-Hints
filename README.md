# CSharp-Hints

## Reflection 
### InvokeMethod
Call method from genetic subclass (you know what is your parent class)
```
var parent = GetSubClass() as ParentClass;
string command = parent.GetType().InvokeMember("ToCommand", BindingFlags.InvokeMethod, null, parent, null);
```

