<div dir=rtl align=right>
# enum

- عبارة عن نوع مبني في اللغة وهو من نوع `value type`
- تعرف نوع من الثوابت التي لا تتغير.
- يتم تعريفه خارج الـ `main`
- يمكن تغيير القيم الافتراضية للعناصر داخل `enum`
- يمكن تنفيذ operators على القيم الموجوة داخل `enum` لكن الرمز يكون مكرر مرة واحدة فقط بخلاف `if` 

###مثال:
المثال التالي يوضح كل ماسبق

<div dir=ltr align=left>

```
using System;

namespace enumKeyword
{
	class Program
	{
		enum days
		{
			Sunday,
			Monday,
			Tuseday,
			Wedensday,
			Thursday,
			Friday,
			Saturday
		}

		enum border: byte
		{
			Left =1,
			Right = 2,
			Top = 10,
			Bottom = 11
		}

		[Flags]
		enum BorderSide
		{
			None=0,
			left=1,
			right=2,
			top=10,
			bottom=12
		}

		ststic void Main(string [] args)
		{
			int WeekStart = (int) days.Sunday;
			int WeekEnd = (int)days.Friday;
			days sun = (days) WeekStart;
			Console.WriteLine("Sunday {0}", WeekStart);

			int i = (int) border.Right;
			border side = (border) i;
			bool leftOrRight = (int) side;
			if(leftOrRight <2)
			{
				Console.WriteLine("You are on the left side");
			}

			BorderSide LeftRight = BorderSide.left | BorderSide.right;
			string formatted = LeftRight.ToString();
			Console.WriteLine(formatted);

		}

	}
}
```