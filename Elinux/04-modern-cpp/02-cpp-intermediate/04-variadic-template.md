```
create function that take more than one argument with different data types
1. here is if the arguments from same type, would have used variadic functions
2. so here we use variadic templates 
```
### who decide what number of arguments 
the caller of the function template ---> accordingly, the compiler make the suitable definition for specified types

### Implementing types 
1. Tail Recursion  std=c++11
2. folding expression std=c++17

### How would argument be passed
1. first, the base number of argument is defined in requirements
2. second, create template parameters for the base
3. third, create another parameters for the rest of arguments using something called parameter packing `...` three dots ---> list of zero or more than one element

## 
### Tail Recursion Implementation Example
```cpp

```




### programming by contract
contract with the caller to use this template with these specified types in documentation

![[4-template_static_assertion.png.png]]



assert