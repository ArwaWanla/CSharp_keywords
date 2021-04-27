<div dir="rtl">

# in

- عبارة عن كلمة اساسية تقوم بتمرير`arguments` عن طريق المرجع `reference` لكن دون تعديل قيمها. 
- تشبه الكلمات المفتاحية `ref` و  `out` لكنها لا تسمح بتعديل قيم المتغيرات الممرة لداخل الدالة.
- اشهر استخدام اعرفه لها هي مع  `foreach loop` بحيث انها تسمح للمستخدم بالوصول الى عناصر مصفوفة ، على سبيل  المثال، لكن لايمكن تعديل اي من قيم عناصر هذه المصفوفة.
- المثال التالي يقوم بطباعة عناصر مصفوفة الفواكه باستخدام `foreach loop` والتي تستخدم `in` للمرور على عناصر المصفوفة وطباعتها.

<div dir="ltr" align =left>

```
using System;

namespace Test
{
    class Program
    {
        static void Main(string[] args)
        {
            string[] fruits = { "apple", "orange", "banana", "watermelon" };

            foreach (var fruit in fruits)
            {
                
              Console.WriteLine(fruit);
                
            }
           
        }
    }
}

```