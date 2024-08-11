### how to create constant member in a class
- compile-time constant [value is known at compile time]
	- constexpr (ensure compile time evaluation)
	- const -> (must be initialized with constant expression(a value that is known and computable at compile time) that is evaluated at compile time)
- runtime constant
	- const -> initialized with value is not known at compile time
#### in class design:
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
* const static with data member can be initialized inside the class for types of integers and enums and this is compile time constant, other types requires evaluations must initialized outside the class and this is runtime constant
* The non-static `const` member `arraySize` is initialized separately for each object, and its value is not available at compile time for array allocation.



## member initializer list
- is good when member data is object ---> enhance performance 
- when you define for example: string name in class 
- and make an object the default constructor is called first and and when provide an argument for this name via equal sign


### initializer_list
- can not use list initialization with it only equal operator = and copy constructor () cause we do not initialize here we are copy the reference to the underlying array.
