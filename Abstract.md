# Abstract

- `abstract` is a modifier that indicates that the thing being modified haas a missing or incomplete implementation. When we use it to before class declaration , we are saying this class is intended to be the base of other classes.

- `abstract` classes have the following features:
		- cannot create an object of that class.
		- the children classes of `abstract class` must do the implementation of `abstract` method in the base class. 
- Example:

```

using System;

namespace Day015session1_assignments
{
    class Program
    {
        public abstract class Shape
        {
            public abstract int ShapeArea();
        }

        public class Circle: Shape
        {
            int r;

            public Circle (int side)
            {
                this.r = side;
            }

            public override int ShapeArea()
            {
                return r * r;
            }
  
        }
        static void Main(string[] args)
        {
            Circle c = new Circle(4);
            Console.WriteLine("The area of Circle = "+ c.ShapeArea());
        }
    }
}

```
