## meta-programming 
- a programming paradigm (approach) like: OOP, procedural.
- make programs (compiler) generate code based on other programs as input
- basically, writing code that write (cause to be written) more code.
- writing code without writing code, when things are not clear 
- HOW? 

![[1-templates.svg]]


## **Templates** 
- cpp provide us with templates to help in meta-programming 
- operate with generic programming ---> generic data types
- not real code, just description that will be created concrete based on the data types you provide later.
- HOW???? Writing a code, the compiler understand it, based on what type of data using, it generate the code for that at ***the compile time***

### Types 
- function template 
- class template 
### (Function Template ) Structure 
```cpp
template <typename T> //template parameters 
T getMax (T num1, T num2)  //template function parameters 
{
	return (num1>num2)?num1:num2;
}

getMax<int>(15,20); //tempalte instantiation   //template function call
```
##### typename  --->  
- keyword to indicate that T represents a type 
- way to tell the compiler that T is a placeholder for the type determined in template instantiation
#### Template Instantiation --->
- create definition from the template
- as for template function: creation of a concrete function with the specific data type 
- as for class template : creation of concrete type with specific data types
==note== 
- here we are not creating an object or instance but an specification 
- ---> object ---> == anything reserved in memory
- ---> instance ---> == object with specific type reserved in memory
- concrete ---> mean with implementation 

![[2-template-instantiation.svg]]
```

```

---
#### Type Specification

`getMax<int>(15,20)`, 
you can either write the type explicitly, known as explicit type specification,
or allow the compiler to deduce it from the template function arguments, a process called **Template Argument Deduction**.

--- 

### linker error issue
- when separate the the template definition from the call that make instantiation, an issue occur because the instantiation happen at compile time 
- the template implementation should exist within the file making call of
- include the template declaration and definition in same header file


#### Template Specialization 
- Template specialization lets templates deal with special cases. for a particular combination of template parameters
- <mark style="background: #ABF7F7A6;">example</mark>, say you have a template that sum two values, but if the two values were string output the length of them
- usually, <mark style="background: #5EFF00A6;">used with user-defined-types or complex types </mark>
- explicit specialization ---> declaration definition (define all template parameters )
- partial specialization ---> declaration definition (define part of template parameters)


```cpp
#include <iostream>
#include <string>
template <typename T>
auto sum(const T& x, const T& y)
{
	return x + y ;
}

// template specialization with strings 
template <>
auto sum(const std:string&x, const std::string& y)
{
	return x.length() + y.length() ;
}

int main()
{
	std::cout << sum (10, 20);
	std::cout << sum (10.5, 20.3);
	std::cout << sum ("Mhmd", "Reda");
	return 0;
}
```

### Note 
1. make sure the data type of he specialization is same as the the general template declaration
2. in specialization you define set of parameters types
3. two types of specialization ---> <mark style="background: #FF5582A6;">study more</mark>



## <mark style="background: #FF5582A6;">study later</mark>
1. overloading vs specialization
2. i think overloading preferred # template parameters
3. specialization when same numbers but extend functionality to certain data type


```cpp
template <> void sum <int>(const int&, const int&);  //explicit specification
template void sum <int>(const int&, const int&);   // explicit instantation 

```

![[3-template-instantiation-speciaalization.png.png]]



```cpp
/**
*auto vs decltype
*/
int x = 10;
double y = 10.2;
//decltype(expression) var; cpp std 11
auto r = x+y; //r is double
decltype(x+y) xytype = x+y;
```