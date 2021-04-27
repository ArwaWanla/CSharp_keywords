<div dir=rtl align = right >

# virtual 

- هي عبارة عن معدل (modifier ) يقوم بالتعديل على الدوال(methods) التي تنشأ في `class` الاب.
- الغرض من هذا المعدل هو ترك المجال للابناء (`derived classes `) لحرية التعديل على هذه الدالة عند وراثتها من الكلاس الاساسي.
- المثال التالي عبارة عن انشاء كلاس shape رئيسي ومن ثم انشاء ابناء يرثون خصائص الكلاس الرئيسي.

<div dir=ltr align = left >

```
using System;

namespace test
{
    class Program
    {
        class Shape
        {
            public double lenght;
            public double width;

            public Shape()
            {

            }
            public Shape(double l, double w)
            {
                lenght = l;
                width = w;
            }

            public virtual void area(double length,double width)
            {
                double Area = length * width;
                
            }
        }

        class Square: Shape
        {
            public Square()
            {

            }
            public Square(double squareLength, double squareWidth):base(squareLength, squareWidth)
            {
                lenght = squareLength;
                width = squareWidth;
            }

            public override void area(double length, double width)
            {
                double area = length * 2;
                Console.WriteLine("the area of Square is :"+ area);
            }
        }

        static void Main(string[] args)
        {
            Square s = new Square();
            s.area(4.9,4.9);
        }
    }
}

```