# `base`

- it is used to access the parent/ base class fields when is has children classes. 
- for instance, when we declare a Child class we do as the following:
```
class Childe : Parent
```
this means that the attributes of Parent can be accessed from Child (Parent is the base).

- Another case we use `base` key word is used to specify the base-constructor when creating instances of the base class. 

example:
```
namespace Day015session1_assignments
{
    class Program
    { 
    lass Person
        {
            //Data
            public string Name;
            public int Id;
            public int Age;

            //Constructor
            public Person(string name, int age)
            {
                this.Name = name;
                this.Age = age;
            }

            public virtual void printInfo()
            {
                Console.WriteLine("Welcome to class");
            }
        }

        class Student : Person
        {
            public int id;
            public string shoolName;

            public Student(string name, int age,int ID, string SN) : base (name, age)
            {
                this.id = ID;
                this.shoolName = SN;
            }

            public override void printInfo()
            {
                base.printInfo();
                Console.WriteLine("this is the student info name{0}, age {1}, ID{2}, School Name: {3}", Name,Age,id, shoolName);
            }
        }
        static void Main(string[] args)
        {
            Student s = new Student("Arwa", 29, 2222, "Fourth High-Shcool");
            s.printInfo();
        }
    }
}
```
