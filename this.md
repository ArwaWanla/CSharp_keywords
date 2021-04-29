<div dir=rtl align=right>
# this

- هي كلمة تشير الى المثيل الحالي من الكلاس  وكذلك تستخدم كمعدل للمدخل الاول لطريقة الامتداد.

###المثال التالي يوضح فكرة `this`في الكلاس
<div dir=ltr align=left>

```
public class Employee
{
    private string name;
    private int phoneNumber;

    public Employee(string name, int phoneNumber)
    {
        
        this.name = name;
        this.phoneNumber = phoneNumber;
    }
}
```
<div dir=rtl align=right>
###المثال التالي يوضح فكرة `this` لتعديل امتداد كلاس رئيسي

<div dir=ltr align=left>

```
using System;

namespace staticCode
{
	public static class stringHelper
	{
		public static bool IsCapitalized(this string str)
		{
			return char.IsUpper(str[0]);
		}
	} 

	class Program
	{
		static void Main(string [] args)
		{
			string message = "Welcome to c#";
			if(message.IsCapitalized())
			{
				Console.WriteLine("Capitalized");
			}
		}
	}
}
```