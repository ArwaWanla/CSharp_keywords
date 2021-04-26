# `as`

- `as` operator is used to convert Object(Type) to another (Type). 
- Object can be `nullable`such as string. `int` type is non-nullable. so, for example the following lines will give error:
```
string str1 = "222";

 object obj1 = str1;

 var name2 = obj1 as int;
```
- returns Object if compatible and `null` when Object is  not.
- example:

```
string str1 = "Arwa222";

 object obj1 = str1;

 var name2 = obj1 as string;

 if (name2 != null)
     Console.WriteLine("Successful");
```