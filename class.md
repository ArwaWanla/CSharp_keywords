# class

- type class is considered as a reference type.
- when declaring a variable of class, the variable will be assigned to the reference of that class which is null at the beginning before creating an object of the class.
- `new` will create an object of the class and the variable will be assigned the reference of the object in the memory when created. 
- c# gives `class` as a tool to create a data type the user wants to build. For example, a student can have ID number, name, age, degree, etc. All of these attributes are different data type. So, `class` can solve or package these data types under a name such as `Student`
- Example:
```
namespace Day015session1_assignments
{
    class Program
    {
    class Student
        {
            //Data
            public string Name;
            public int Id;
            public int Age;

            //Constructor
            public Student(string name, int d, int age)
            {
                this.Name = name;
                this.Id = Id;
                this.Age = age;
            }

            public void printInfo()
            {
                Console.WriteLine("Welcome to class");
            }
        }
   
        static void Main(string[] args)
        {
            Student s = new Student("Arwa", 2222, 29);
            s.printInfo();
        }
    }
}
```

