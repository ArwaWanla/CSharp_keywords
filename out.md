<div dir="rtl">
# out
- يعتبر نوع من معدلات modifier لمدخلات الدوال التي ينشئها المستخدم. 
- يسمى كذلك  value typeوذلك لانه يمكن استخدامه لتعديل قيمة متغير من الدالة مباشرة. ولكن هناك اختلاف عن النوع `ref` في التالي:
 	- يمكن تعريف المتغير ونوعه دون اسناد قيمة له في البداية.
 	- عند تمريره لدالة ما، يجب اسناد قيمة له قبل الخروج من الداله.
- المثال التالي عبارة عن دالة تستقبل عددين ومتغير من النوع intوتقول باسناد قيمة الجمع لهذا المتغير.



<div dir="ltr" align =left>

``` 
using System;

namespace Test
{
    class Program
    {
        static void Main(string[] args)
        {
            //int c;
            //sum(1, 9, out c);
            //Console.Write(c);

            int x=5;
            Console.WriteLine(x);
            mult(ref x);
            Console.WriteLine(x);
            //output: 5
                    //25
        }

        static void mult(ref int r)
        {
            r = r * r;
            
        }
        static void sum(int a, int b, out int c)
        {
            c = a + b;
        }
       
    }
}
