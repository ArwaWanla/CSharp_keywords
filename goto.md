# `goto`

- The `goto` statement transfers the program control directly to a labeled statement.
- it used to jump from a block of code to another.

example:

```
int count = 0;

print:
	Console.WriteLine("hello");
    count++;
if (count < 5)
    goto print;
                
```