<div dir="rtl">

# continue

- هي عبارة عن جملة تقوم بالقفز الى الدورة او التكرار التالي `loop ` سواء كانت `do while` او `for`او `while` او `foreach`
- المثال التالي عبادة عن مصفوفة مكونة من اسماء اشخاص. اذا لم يكن اسم الشخص "صالح" فانها تقفز للتكرار التالي. 

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
                if (name != "Saleh")
                {
                    Console.WriteLine(name);
                    continue;
                }
            }
        }
    }
}

        


```