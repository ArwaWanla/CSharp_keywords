# `delegate`

- it is a type that used to encapsulate methods which interfaces are the same. 
- let's assume we have four functions for basic math operations: sum, sub, must, div. All four functions receive two integer variables and return an integer. So, we can create a `delegate` as long as functions respect the interface of the `delegate function`.
- it provides flexibility in a way that it will be pointing to all four function, for instance, at one time. However, it will return the output of the last function it points to. 

example:
```
using System;

namespace Day012_session2_delegate
{
    class Program
    {
       
        static void Main(string[] args)
        {
            DoAction ma = sum;
            int result = ma(2, 4);

            ma = sub;
            result = ma(5, 2);

            DoAction[] operations = { sum, sub, mult, div };
        }

        public delegate int DoAction(int a, int b);
        public static int sum(int a, int b)
        {
        return a + b;   
        }
        public static int sub(int a, int b)
        {
            return a - b;
        }
        public static int mult(int a, int b)
        {
            return a * b;
        }
        public static int div(int a, int b)
        {
            return a / b;
        }
    }
}

```