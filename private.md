<div dir=rtl align=right>
# private
- هو معدل يضيق نطاق الوصول الى الدوال او المتغيرات في كلاس معين.بحيث ان اي عنصر يستطيع الوصول الي متغير `private`  فقط داخل الكلاس الموجود فيه.

- مثال التالي يوضح الفكرة.لايمكن الوصول الي المتغير `Bedroom` لانه خاص داخل الكلاس فقط

<div dir=ltr align=left>

```
using System;

namespace test
{
    class Program
    {
        class Me
        {
            public string name;
            private string Bedroom;
        }

        static void Main(string[] args)
        {
            Me person = new Me();
            person.name = "Arwa";
            
        }
    }
}
```