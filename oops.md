1) What is Procedural programming ? </br>
   It is a list of instructions in a single block and suitable only for small programs.
2) What is Modular programming ? </br>
   Modular program is divided into functions and each function has a clear purpose. The limitation is that it is difficult to relate it with real world problems. As modular      programming needs more of our data to be global so that it can be accessed across the program but it has its own limitations. It will create a mesh which is difficult to      modify. The reason for such a mess is that the data and functions are separate. So, we need to bind our data and functions that's what we do in object oriented approach by    creating class.
3) Do class takes any space ? </br>
   Class does not occupy any space but object does. Class is just a blueprint.
4) What is class ? </br>
   Class is a user defined datatype, which holds its own data members and member functions. Class helps in code reusability.
5) How we call member variables and member functions of a class ? </br>
   house h1;   ----------->  // this is how we create an object of a class </br>
   h1.len;     ----------->  // this is how we can access member variable of a class </br>
   h1.area();  ----------->  // this is how we can access member functions of a class </br>
6) By default which access specifier is there in class ? </br>
   By default, access specifier is private. Private means member variables and member functions can be used within the class only. Make member variables as private so that it    can't be accessed outside class making it safe and make your member functions as public so that your class function can be accessed from outside and the function can          access member variables.
7) What happens when we create an object ? </br>
   Any entity that has state and behavior is known as an object. </br>
   Here, state means data and behavior means functionality. </br>
   Object is a runtime entity, it is created at runtime. </br>
   Whenever we create an object member variables will get fresh or new space each time while member functions are shared between them.
8) What is encapsulation ? </br>
   The process of combining member variables and member functions is called encapsulation. Encapsulation is wraping up variables and methods in class. It helps in data hiding    with the help of access specifiers. Security of data is possible in this way.
9) What is abstraction ? </br>
    Hiding internal details and showing functionality is known as abstraction. Abstraction is hiding complicated things from user like a coffee machine. In C++, we use           abstract class and interface to achieve abstraction.
10) Difference between abstraction and encapsulation ? </br>
    https://www.geeksforgeeks.org/difference-between-abstraction-and-encapsulation-in-c/
11) What is polymorphism ? </br> 
    Function Overloading. 2 ways: one by changing number of arguments, one by changing datatype. Polymorphism helps in reducing the complexity and length of code.
12) What is data hiding ? </br>
    Class2 is child of class1 then class2 can use public and protected member variables. If class2 is not child of class1 then class2 can only use public member variables
     like in main class we can't use protected or private member variables. With this approach, we can hide our data. This is called data hiding.
13) What is constructor ? </br>
    Constructor is having same name as class and they don't return anything. A a_obj(28); // initialise data
14) Why do we need constructors ? </br>
    Programmers may forgot to initialise data members in object. When there are many objects, then we need to call set data for each object.
15) What happens when constructor is called ? </br>
    When constructor is called, it first allocates memory to data members and then initialise it.
16) Tyeps of constructor ? </br>
    Non-parameterised constructor/default constructor: that does not take any argument. data member set with default value so do not need to pass arguments. If you don't         create a constructor then default constructor will work and set the data members with garbage value.
    Parameterised constructor: that takes some arguments. </br>
    Copy constructor: They are used to create new objects from existing objects. </br>
    A a_obj2(a_obj1); </br>
    A(A &a_obj1) {    </br>
        age = a_obj1.age;  </br>
    }  </br>
17)  What is Overloaded constructor ? </br>
     overload parameterised and non-parameterised constructor. </br>
     A(int x = 0) {  // default value set in parameter only </br>
        age = x; </br>
     } </br>
18)  How can we create function outside the class ? </br> 
     We can declare a function in class and its definition outside the class as </br>
     returntype classname::func(arguments) { } where :: is scope resolution. </br>
19)  What is Operator overloading ? </br> 
     When we make operators like +,-,/,* work for user defined datatypes likes objects and structures.
20)  How can we differentiate overloading of pre and post increment ? </br>
     In post increment overloading we write "int" word in arguments to differentiate it with pre increment operator overloading.
21)  What is inheritance ? </br>
     Inheritance is acquiring properties of another class. Inheritance reduces duplicate code, increases code reusability and it helps in better organisation of code. It is        used to achieve runtime polymorphism.
22)  What happens if we we execute " derived d" and the derived class has no constructor ? </br>
     If derived class has no constructor then it will call the constructor of base class (ONLY APPLICABLE FOR DEFAULT CONSTRUCTOR) 
23)  What happens if we we execute " derived d(9)" and the derived class has no parameterised constructor ? </br>
     It will give error.
24)  What happens if we call "derived d" and derived class has its default constructor ? </br>
     when we call default constructor of derived class it first calls the base class default constructor and then default constructor of derived class.
25)  What happens if we call "derived d(9)" and derived class has its parameterised constructor ? </br>
     When we call parameterised constructor of derived class it first calls the base class default constructor (not parameterised constructor of base class) and then              parameterised constructor of derived class.
26)  How can we call parameterised constructor of base class ? </br>
     derived(int d) : base(d)
27)  What is Function overriding? </br>
     Derived class object would call the function of derived class if same function exists in both classes (i.e. base and derived class)
28)  How can we call same function of base class through derived class object if derived class has same function already ? </br>
     If we write base::Msg() in derived class that has already a function named Msg() then it will call the base class Msg function.
29)  What is isA relationship ? </br> 
     Inheritance
30)  What is hasA relationship ? </br>
     It is implemented using objects, we create objects of class whose function we need to use.
31)  What is the difference between isA and hasA relationship ? </br>
     isA relationship is based on inheritance while hasA relationship is based on objects. </br>
     isA relationship expose all public data of base class but hasA relationship does not expose all data but it uses relevant data.
     isA relationship is static binding (compile time) while hasA relationship is dynamic binding (run time).
     isA relationship is used when we can inherit something while hasA relationship is used when we can't inherit most of the things.
32)  What is public inheritance ? </br>
     Default inheritance is private. </br>
     child and grandchild class would not be able to access private members but be able to access both protected and public members. </br>
     protected would be inherited as protected and public would be inherited as public in child and grandchild class.
33)  What is protected inheritance ? </br>
     (class derived : protected base) </br>
     protected and public in parent class would be inherited as protected in child and grandchild class.
34)  What happens when we create base class pointer and set it with derived class object like base * ptr; ptr = new Derived(); ? </br>
     The pointer is of base class but object is of derived class but it will not throw any error as base class is compatible with derived class. If we treat base class as car      and derived class as advanced car like ferrari, then we are saying that we are sitting in a normal car pointing towards a ferrari and saying that our car is also              ferrari. We can't access the member functions of derived class with base class pointer.
35)  What is virtual function ? </br>
     It is a function existing in class that can't be used. Program that appears to be calling function of one class but in reality maybe calling function of different class.
     By making base class function virtual by appending "virtual" word in function we can tell compiler that show() is my derived class function not base class function.
36)  What is Late binding/ Dynamic binding ? </br>
     Compiler defer the decision until the program is running. And at runtime when it comes to know which class is pointed by ptr, then appropriate function will be called.
37)  What is abstract class ? </br>
     Abstract class is used when we never want to instantiate object of BASE class. </br>
     When we do (virtual returntype funcname() = 0;) then it becomes a pure virtual function and if a pure virtual function exists in a class then it becomes an abstract          class. Pure virtual function does not have a body. </br>
     Abstract class exists only to "ACT" as parent of derived class. It itself has no functionalities. 
38)  What are Destructors ? </br>
     It destructs the objects of classes. </br>
     It can be defined only once in a class. </br>
     Like constructors, it is invoked automatically.</br>
     They are used to deallocate memory. </br>
     They are used to clean up the class objects and class members. </br>
     They are called when the object is out of scope or we are explicitly deleting the object.
39)  How to destroy whole object using base class pointer and derived class object ? </br>
     When we create pointer of base class and object of derived class (base * b = new derived;) then only base class functionalities can be accessed. </br>
     delete b then only base class deconstructor is called so whole object is not destroyed. </br>
     But if we create our deconstructor as virtual ~base() { } (appending virtual in front) then deconstructor of both base and derived class is called and whole object is        destroyed.
40)  What is friend function ? </br>
     When a function is outside the class then it can access only public variables but if we make it friend function then it can access all 3. </br>
     It can be declared either in the private or the public part.</br>
     It cannot be called using the object as it is not in the scope of that class.
41)  Syntax of friend function ? </br> 
     friend returntype funcname();
42)  What is friend class ? </br>
     Friend classes can use and access the features and functionalities of each other. </br>
     Friend class can access private data members of other class. Let's say in class A we write friend class B; then through class B we can access functionalities of class A.
43)  What are static member variable ? </br>
     Each object will create separate space in memory </br>
     Static member would be allocated memory only once and the memory is shared by all objects of class </br>
     Static data members belong to a class and it is common to all objects. </br>
     We need to write "static int stat;" in class to define it and then outside class write "int classname :: stat = 0;"  (type of global declaration) </br>
     We can print static variable using class or object like objectname.stat or classname::stat
44)  What is static member function ? </br>
     Static member function is a special function which can only access static member variable
45)  C++ supports 5 types of inheritance : Single, Multiple, Hierarchical, Multilevel, Hybrid 
