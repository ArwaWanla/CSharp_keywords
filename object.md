<div dir=rtl align=right>
	
# Object

- هو نوع من البيانات المعرفة مسبقا في لغة سي شارب. 
- يمكن تعيين اي قيمة من اي نوع من المتغيرات لـ`object` 
- قيمتها الافتراضية هي `null` 
- عند تحويل اي نوع من المتغيرات الى النوع `object` فهذا يعني ان المتغير يتم تغليفه والعكس.

### مثال  :
المثال التالي يوضح مفهوم `object`

<div dir=ltr align=left>

```
using System;

namespace as_keyword
{
    class Program
    {
        static void Main(string[] args)
        {
            object value = 10;
            string anotherValue = (string)value;//casting

            Console.WriteLine(anotherValue);


            string anotherValue = value as string;
            Console.WriteLine(anotherValue);
			}
	}
}      

```
