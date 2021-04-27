<div dir="rtl">

# break

- هي عبارة عن جملة تقوم بالقفز خارج اقرب `loop ` تكون موجودة فيه او  `switch` بعد ذلك يعود البرنامج الى السطر التالي من مكان تواجد `break`
- المثال التالي عبارة عن مصفوفة اسماء، نطبع الاسماء باستخدام `loop`،اذا كان اسم الشخص صالح فان الدورة ستتوقف وتقفز للسطر التالي من الدورة

<div dir="ltr" align =left>

```
using System;

namespace Test
{
    class Program
    {
        static void Main(string[] args)
        {
            string[] names = { "Ahmad", "Adel", "Saleh", "Waleed" };

            foreach (var name in names)
            {
                if (name == "Saleh")
                {
                    Console.WriteLine(name);
                    break;
                }
            }
            Console.Write("THE person Saleh is found");
        }
    }
}

```