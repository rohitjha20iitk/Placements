1) What is Procedural programming ? </br>
   It is a list of instructions in a single block and suitable only for small programs.

2) What is Modular programming ? </br>
   Modular program is divided into functions and each function has a clear purpose. The limitation is that it is difficult to relate it with real world problems. As modular      programming needs more of our data to be global so that it can be accessed across the program but it has its own limitations. It will create a mesh which is difficult to      modify. The reason for such a mess is that the data and functions are separate. So, we need to bind our data and functions that's what we do in object oriented approach by    creating class.
   
3) Do class takes any space ? </br>
   Class does not occupy any space but object does. Class is just a blueprint.
   
4) What is encapsulation ? </br>
   The process of combining member variables and member functions is called encapsulation.
 
5) How we call member variables and member functions of a class ? </br>
   house h1;   &nbsp  // this is how we create an object of a class </br>
   h1.len;     &nbsp  // this is how we can access member variable of a class </br>
   h1.area();  &nbsp  // this is how we can access member functions of a class </br>
   
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
42)  isA relationship = Inheritance
43)  hasA relationship = implemented using objects we create objects of class whose function we need to use.
44)  isA relationship is based on inheritance while hasA relationship is based on objects.
45)  isA relationship expose all public data of base classes but hasA relationship does not expose all data but it uses relevant data.
46)  isA relationship is static binding(compile time) while hasA relationship is dynamic binding (run time).
47)  isA relationship is used when we can inherit something while hasA relationship is used when we can't inherit most of the things.
48)  child and grandchild class would not be able to access both private bur be able to access both protected and public.
49)  protected would be inherited as protected and public would be inherited as public in child and grandchild class.
50)  protected inheritance (class derived : protected base) protected and public in parent class would be inherited as protected in child and grandchild class.
51)  Base class pointer and derived class object: Base * ptr = NULL; ptr = new Derived();  The pointer is of base class but object is of derived class but it will not throw any error as base class is compatible with derived class.
52)  If we treat base class as car and derived class as advanced car, then we are saying that we are sitting in a normal car pointing towards a ferrari and saying that our car is also ferrari. We can't access the member functions of derived class with base class pointer.
53)  Virtual function is a function existing in class that can't be used.
54)  Virtual functiom : Program that appears to be calling function of one class but in reality maybe calling function of different class.
55)  By making base class function virtual as mentioned in pics, we can tell compiler that show() is my derived class function not base class func.
56)  Late binding/ Dynamic binding: Compiler defer the decision until the program is running. And at runtime when it comes to know which class is pointed by ptr, then appropriate function will be called.
57)  When we place virtual word in front of a function in base class then it becomes a virtual function.
58)  Abstract class is used when we never want to instantiate object of BASE class.
59)  When we say (virtual returntype funcname() = 0;) then it becomes a pure virtual function and if a pure virtual function exists in a class then it becomes an abstract class
60)  Abstract class exists only to "ACT" as parent of derived class. It itself has no functionalities.
61)  pure virtual function does not have a body.
62)  Destructors are used to deallocate memory.
63)  They are used to clean up the class objects and class members.
64)  They are called when the object is out of scope or we are explicitly deleting the object.
65)  When we create pointer of base class and object of derived class (base * b = new derived;) then only base class functionalities can be accessed.
66)  delete b then only base class constructor is called so whole object is not destroyed.
67)  But if we create our deconstructor as virtual ~base() { }  (appending virtual in front) then deconstructor of both base and derived class is called and whole object is destroyed.
68)  When a function is outside the class then it can access only public variables but if we make it friend function then it can access all 3.
69)  friend returntype funcname();
70)  Friend classes can use and access the features and functionalities of each other.
71)  Friend class can access private data members of other class. Let's say in class A we write friend class B then through class B we can access functionalities of class A.
72)  Each object will create separate space in memory.
73)  Static member would be allocated memory only once and the memory is shared by all objects of class.
74)  Static data members belong to a class and it is common to all objects.
75)  we need to write static int stat in class to define it and then outside class write int classname :: stat = 0;  (type of global declaration)
76)  We can print static variable using class or object like objectname.stat or classname::stat
77)  static member function is a special function which can only access static member variable
