<div dir=rtl align= right>

# override

- يستخدم هذا المعدل لتعديل الوصول الى دوال داخل الكلاس والتي تكون `virtual`و `abstract`  والموجودة في الكلاس الرئيسي بحيث تستطيع الكلاسات التي ورثت من الكلاس الرئيسي التعديل على الدالة.
- مثال:
انشاء كلاس `مربع` من الكلاس الرئيسي `شكل`  بحيث يحتوي الكلاس الرئيسي على دالة من نوع `abstract`  والتي تستوجب على من يرث تنفيذ الدالة

<div dir=ltr align= left>

```
using System;

namespace test
{
    class Program
    {
        abstract class Shape
        {
            public double length;
            public double width;

            public Shape()
            {

            }
            public Shape(double l, double w)
            {
                length = l;
                width = w;
            }

            public abstract double area();
        }

        class Square: Shape
        {
          
            public Square(double squareLength, double squareWidth):base(squareLength, squareWidth)
            {
                length = squareLength;
                width = squareWidth;
            }

            public override double area()
            {
                double area = this.length * 2;
                return area;
            }
        }

        static void Main(string[] args)
        {
            Square s = new Square(5.1,5.1);
            Console.WriteLine("the area of square is: {0}", s.area());
        }
    }
}

```