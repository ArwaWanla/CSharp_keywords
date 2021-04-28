<div dir=rtl>
# public
- هو معدل وصول على الدوال والبيانات الموجودة في كلاس معين.
- لا توجد اي قيود باستخدام هذا المعدل بحيث يمكن الوصول اليها من اي مكان في البرنامج.
- مثال التالي يوضح فكرة `public`

<div dir=ltr align=left>

```
using System;

namespace test
{
    class Program
    {
        public class Fruit
        {
            public string color;
        }

        class Apple: Fruit
        {
            public string type;

            

            public void fruitInfo()
            {
                Console.WriteLine("The apple type is {0}, color is {1}",type, color);
            }
        }

        static void Main(string[] args)
        {
            Apple apple = new Apple();
            apple.type = "Gala";
            apple.color = "Red";
            apple.fruitInfo();

        }
    }
}

```