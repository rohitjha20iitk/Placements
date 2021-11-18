1) Procedural programming: list of instructions in a single block. Suitable only for small programs.
2) Modular programming: procedural program is divided into functions and each function has a clear purpose. Limitation: Difficult to relate it with real world problems.
3) As modular programming needs more of our data to be global so that it can be accessed across the program but it has its own limitations.
4) It will create a mesh which is difficult to modify. The reason for such a mess is that the data and functions are separate.
5) So, we need to bind our data and functions that's what we do in object oriented approach by creating class.
6) The process of combining member variables and member functions is called encapsulation.
7) Class does not occupy any space but object does. Class is just a blueprint.
8) Object creation : house h1; where house is class name and member function is called as h1.area();
9) By default, access specifier is private. Private means member variables and member functions can be used within the class only.
10) Make member variables as private so that it can't be accessed outside class making it safe and make your member functions as public.
11) Whenever we create an object member varibales will get fresh or new space each time while member functions are shared between them.
12) class2 is child of class1 then class2 can use public and protected member variables only not private member variable.
13) If class2 is not child of class1 then class2 can only use public member variables like in main class we can't use protected or private member variables.
14) With this approach, we can hide our data. This is called data hiding.
15) Class is a user defined datatype, which holds its own data members and member funbctions. Class helps in code reusability.
16) Encapsulation is wraping up variables and methods in class. It helps in data hiding with the help of access specifiers. Security of data.
17) Polymorphism : Function Overloading. 2 ways: one by changing number of arguments one by changing datatype. Polymorphism helps in reducing the complexity and length of code.
18) Abstraction is hiding complicated things from user like a coffee machine.
19) https://www.geeksforgeeks.org/difference-between-abstraction-and-encapsulation-in-c/
20) Constructor is having same name as class and they don't return anything. A a_obj(28)
21) Need for constructor: programmers may forgot to initialise data members in object. When there are many objects, then we need to call set data for each object.
22) When constructor is called, it first allocates memory to data members and then initialise it.
23) Non-parameterised constructor/default constructor: that does not take any argument. data member set with default value so do not need to pass arguments. If you don't create a constructor then default constructor will work and set the data members with default or garbage value.
24) Parameterised constructor: that takes some arguments.
25) Copy constructor are used to create new objects from existing objects. A a_obj2(a_obj1) // copy constructor
26)  A(A &a_obj1) { age = a_obj1.age; }
27)  Overloaded constructor: overload parameterised and non-parameterised constructor. A(int x = 0) { age = x;} default value set in parameter only.
28)  We can declare a function in class and its definition outside the class as returntype classname::func(arguments){ } where :: is scope resolution.
29)  Operator overloading: when we make operators like +,-,/,* work for user defined datatypes likes objects and structures.
30)  Operator overloading in details in picture(ss)
31)  How can we differentiate overloading of pre and post increment in post increment overloading we write int in arguments to differentiate it with pre increment overloading.
32)  Base class is parent class and derived class is child class.
33)  Inheritance is acquiring properties of another class.
34)  Inheritance reduces duplicate code, increases code reusability and it helps in better organisation of code.
35)  if derived class has no constructor then it will call the constructor of base class (ONLY APPLICABLE FOR DEFAULT CONSTRUCTOR) 
36)  parameterised constructor will give error.
37)  when we call default constructor of derived class it first calls the base class default constructor and then default constructor of derived class.
38)  when we call parameterised constructor of derived class it first calls the base class default constructor (not parameterised constructor of base class) and then parameterised constructor of derived class.
39)  There is a different way to call parameterised constructor of base class (in photo)
40)  Function overriding: derived class object would call the function of derived class if same function exists in both classes(i.e. base and derived class)
41)  if we write base::Msg() in derived class that has already a function named Msg() then it will call the base class Msg function. In this way we can call Msg function of base class.
42)   
