## <mark style="background: #ABF7F7A6;">OOP: </mark>
<mark style="background: #FF5582A6;">1. </mark>programming paradigm based on objects
### Programming Paradigm
1. [way]  [approach]  [style] of thinking of [designing]  [writing]  [creating] programs.
2. not a language itself.
3. some languages make it easy to support different paradigms.

<mark style="background: #FF5582A6;">2. </mark>provides some features:
	1. Abstraction
	2. Encapsulation
	3. Polymorphism
	4. Inheritance
	5. Re-usability of code

----
## <mark style="background: #ABF7F7A6;">Procedural vs OOP</mark>
### <mark style="background: #FF5582A6;">1. </mark>procedural:
- paradigm based on subroutines
- dividing program into multiple modules and subroutines
- **in terms of design:**
	1- first, we concentrate on the procedures we will follow (tasks, functions, subroutines).
	2- second, we think how to represent the data.
### <mark style="background: #FF5582A6;">2-</mark> OOP:
- based on objects. 
- in terms of design:
	1- first, we think of an object that represents the fundamental data unit.
	2- second, think about the data [attributes]  [properties]  of the object.
	3- third, how to represent the data.
	4- forth, the operations done on these data, which describes user interactions. [interface]
	
---
## <mark style="background: #ABF7F7A6;">Abstraction</mark>: عمليه تسهيل 
1. A feature provides by oop.
2. The process of simplifying complex systems:
	1. concentrate on important aspects.
	2. hide unnecessary information.
3. In computing, the process of representing the information in terms of interfaces with the user to deal with.
- يعني احنا بنقدم لليوز واجهة بيستخدمها من غير بقي ميعرف ايه اللي بيحصل خلف الكواليس
- في الكلاس بيبقي فيه سيكشن للدتا وسيكشن لل methods اللي تعتبر interfaces من ال design فهي اللي اليوز بيستخمدها [developer] علشان يغير ف الداتا.
--- 
## <mark style="background: #ABF7F7A6;">Data Types</mark>:
 - A type in programming refer to:
	1. how much memory needed for data object. 
	2. how the bits are interpreted
	3. determine which operations done on the object.
	[object] ---> anything that is stored in memory.
- so type means ---> memory size and operation.
- for built-in data types, the rules are reserved to the compiler
- for user defined data types, you have the power and flexibility to create new types.
--- 
## <mark style="background: #ABF7F7A6;">Class and Object:</mark>
- class: 
	1. the general definition of an object. [blueprint]
	2. consists of the data representation and the operation [methods] done on the data.
	3. the class in divided into section:
		1. private 
		2. public
		3. protected
	4. the elements inside the class are called members
		1. data members [member variables] ---> attributes.
		2. member functions  ---> methods.
		- these are the names that given to data and methods.
		- member functions in class design are called public interfaces
-----
## <mark style="background: #ABF7F7A6;">Class Design:</mark>
- class specification has two parts: 
  علشان نحدد او نعرف الكلاس كديزاين لازم يكون عندنا 
 ### <mark style="background: #FF5582A6;">1.  </mark> Class Declaration
- provide overview of the class regarding data representation and class interfaces [class method prototypes]
 ### <mark style="background: #FF5582A6;">2. </mark>Class Method Definition 
- provide [supply] method implementation details
- <mark style="background: #D2B3FFA6;">typically c++ programmers do:</mark>
		1. put Class Declaration in header file.
		2. put Class Method Definitions in source code.
		3. make a library whether static or dynamic.
---
## <mark style="background: #ABF7F7A6;"> Encapsulation: </mark> 
<mark style="background: #FF5582A6;">1.</mark> One of OOP features
<mark style="background: #FF5582A6;">2.</mark> binding [combining] the data and the method manipulating on that data into single unit ---> class <mark style="background: #FFB86CA6;"> in order to hide data</mark>. 
<mark style="background: #FF5582A6;">4.</mark> enforce restriction on access the data inside the class to ensure controlled and safe access using class access modifiers [set access control].
#### <mark style="background: #FF5582A6;">5.</mark> Encapsulation and Abstraction
-  since Encapsulation done to hide the data and Abstraction done to hide implementation of functions, we can use Abstraction inside Encapsulation to ensure total hide of implementation details.
<mark style="background: #FF5582A6;">6. </mark>Serve multiple purposes:
	<mark style="background: #BBFABBA6;">1.</mark> data hiding: insulation of data from direct access [data integrity] and needn't to know hoe data is represented.
	<mark style="background: #BBFABBA6;">2.</mark> gathering implementation details and separating them from the abstraction. usually in different source file
	<mark style="background: #BBFABBA6;">3.</mark> hide functional details: put function in private section.
	
---

## <mark style="background: #ABF7F7A6;">Class vs Struct:</mark>
1. Both represent a single unit of encapsulation.
2. look much like the same.
3. the difference in class the default control access is private while in struct is public
4. <mark style="background: #D2B3FFA6;">typically c++ programmers do:</mark>
	1. use class to express class descriptions
	2. restrict struct to only pure-data object (ANA. plain-old data structures or POD structures).
---
## <mark style="background: #ABF7F7A6;">Class Method Definition:</mark>
 1. Method can be defined inside the class using the unqualified name (the name of the method with the class name). 
    like: `update(){/**********/}`
 2. according to class design, Method definitions is written in source code using the qualified name via class scope resolution to identify to which class the method belongs. 
    like:   `class_name::update(){/*********/}`
    
### 3. Inline Method:
- the inline keyword: suggestion to the compiler to copy the content of a function to every place where it called to reduce processor overhead due to context switching.
- in classes:
	1. automatically only small and short functions defined in class declaration become inline functions
	2. in case of separation of method definition and need to use inline, you use <mark style="background: #FFF3A3A6;">rewrite rule</mark> 
			- use prototype in class declaration without `inline`
			- provide definition in same file using `inline` why?
			1. you need the source code for compile each translation unit.
			2. must be defined in each file used in
---

## <mark style="background: #ABF7F7A6;">Class Constructors:</mark>
- Special member function used to initialize class objects.
- some rules:
	1. have the name of the class itself.
	2. have no return type and no void.
	3. called automatically when class object is created.
### <mark style="background: #FFF3A3A6;">Note:</mark>
- not to be confused between data member and contractors parameters there is a convention to use with data member:
	1. to use under-bar suffix to identify data member.
	2. to use m_ prefix with data members.(<mark style="background: #FFF3A3A6;">preferred</mark>)
	3. if used initialization list or this pointer explicitly, there will be no confusion or error.

### Constructors Types:
1. Default constructor:
	1. used when no explicit initialization is provided
	2. c++ automatically provide one implicitly that do nothing when no provided
	3. if there is a parameterized one, you must explicitly provide default constructors on your own, if do not and try to use it [error].
	4. can also be defined as [default argument for para constructors], only one is used
	5. <mark style="background: #D2B3FFA6;">typically c++</mark>:
		- use default constructors to initialize implicitly class data members.
2. Parameterized Constructors.
3. Copy Constructors.
4. Move Constructors.

## <mark style="background: #ABF7F7A6;">Destructor:</mark>
1. special member function used to free deallocated memory from heap
2. rules:
	1. has name of the class prefix with~
	2. has no return type
	3. called automatically after class object lifetime expire with the right brace of scope
3. can not be overloaded 
4. c++ compiler provide implicitly one that do nothing. 

## <mark style="background: #ABF7F7A6;">Const member function:</mark>
- لو عندك class وفيه جواه method بس انت مش عاوزها تغير في ال data member بتاعه ال invoking object اللي عمل call, وعلشان نستخدم const لازم نحطها قبل ال object اللي احنا مش عاوزين نعدل فيه وطبعا هو بيحصله passing implicitly not via method arguments فقالو نضيف syntax جديد.
- const is placed after the parenthesis of the declaration and definition
- const here is a promise not to change the invoking object.
	- void show() const;
	- void CLASS_NAME::show()const{}

## <mark style="background: #ABF7F7A6;">this pointer:</mark>
- a pointer point to the invoking object that is passed implicitly.

## <mark style="background: #ABF7F7A6;">class scope:</mark>
- scope --> place where object is defined
	1. Global scope [file scope] : defined outside any function and namespace
	2. local scope [block/function scope]
	3. class scope: defined inside class ---> all members show each others
		1. in class the unqualified name is used 
		2. outside class the full qualified name is used

----
## <mark style="background: #ABF7F7A6;">How to create constant member in a class</mark>
- compile-time constant [value is known at compile time]
	- constexpr (ensure compile time evaluation)
	- const -> (must be initialized with constant expression(a value that is known and computable at compile time) that is evaluated at compile time) 
- runtime constant
	- const -> initialized with value is not known at compile time
### <mark style="background: #ABF7F7A6;">In class design:</mark>
- constexpr is applied only to static data member and member function (static, non-static)
	- constexpr with member function means the evaluation can be done at compile time  
		- conditions for compile time:
		- 1- the invoking object itself is constexpr
		- 2- the arguments passed are constexpr
		- const Qualification 
		- 3- for non-static member fun to be constexpr, i must be const. it will not change the state of object and this is necessary for compile-time evaluation 
	* constexpr with static data member 
		* the data applied to the class and shared between all objects
		* so you can define static data at compile time without object
		* must be initialized inside the class (in class initialization| default member initialization)
* const static with data member can be initialized inside the class for types of integers and enums and this is compile time constant `also` with float c++98 not allow but c++11 removes restrictions, other types requires evaluations must initialized outside the class and this is runtime constant
* The non-static `const` member `arraySize` is initialized separately for each object, and its value is not available at compile time for array allocation.
* static defined inside class can not be accessed directly via address as no storage is allocated storage
### <mark style="background: #ABF7F7A6;">const class object:</mark>
- can only access const data member and const member function.
- to ensure that object internal is not changed.
