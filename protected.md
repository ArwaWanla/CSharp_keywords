<div dir=rtl align=right>
# protected
- يعتبر نوع من معدلات الوصول والذي يسمح بالوصول الى عناصر المصفوفة الرئيسية ومن يرث منها او يشتق منها.
- ملاحظة مهمة: العنصر المحمي `protected`يمكن الوصول اليه داخل الكلاس المشتق والرئيسي.
- المثال التالي: كلاس الشكل الرئيسي، ومشتق منه كلاس المربع لحساب مساحته.

<div dir=ltr align=left>

```
using System;

namespace test
{
    class Program
    {
        abstract class Shape
        {

            protected int x;
            protected int y;

            public abstract int area(int length, int width);
        }

        class Square: Shape
        {
            public int length;
            public int width;

            public Square(int Length, int Width, int X, int Y)
            {
                length = Length;
                width = Width;
       
            }  

            public override int area(int X, int Y)
            {
                int area = X * Y;
                return area;
            }
        }

        static void Main(string[] args)
        {
            Square s = new Square(2, 2, 3, 4);

            Console.WriteLine("The Area of Square is : " + s.area(3, 4));

        }
    }
}

```