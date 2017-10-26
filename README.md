# CSharp-Hints

## Reflection 
### Invoke Method
Call method from genetic subclass (you know what is your parent class)
```
var parent = GetSubClass() as ParentClass;
string command = parent.GetType().InvokeMember("ToCommand", BindingFlags.InvokeMethod, null, parent, null);
```

### Create Instance
Create instance/object of a class (you know what is the class name)
```
//namespace + ClassName
string fullTypeName = "MyProject.Model.MyClass";
var type = Type.GetType(fullTypeName);
Activator.CreateInstance(type);
```


