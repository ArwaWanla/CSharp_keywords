<div dir=rtl align=right>
    
# params

- هي كلمة تستخدم في تمرير عدد لا متناهي من المتغيرات في الدوال.
- اذا كنا نريد ادخال اكثر من متغير للدالة بالاضافة الى `params` ،يجب انا نضع `params` كاخر مدخل لتمرير المتغيرات للدول . السبب يعود ان `params` لا تسمح بتمرير اي متغير بعدها.
- يجب ان تكون المتغيرات في `params` مصفوفة ذات بعد واحد

### المثال:
- يوضح المثال التالي مفهوم `params`

<div dir=ltr align=left>

```
using System;

namespace ParamKeyword
{
    class Program
    {
        public static void UseParams(params int[] list)
        {
            for (int i = 0; i < list.Length; i++)
            {
                Console.WriteLine(list[i]);
            }
            Console.WriteLine();
        }
        public static void UseParam2(params object [] list)
        {
            for (int i = 0; i < list.Length; i++)
            {
                Console.WriteLine(list[i] + " ");
            }
            Console.WriteLine();

        }
        static void Main(string[] args)
        {
            UseParams(1, 2, 3, 4, 5, 6, 7, 8);
            UseParam2(1, 'a', "test");

            int[] myIntArray = { 5,6,7,8,9};
            UseParams(myIntArray);
        }
    }
}

```
