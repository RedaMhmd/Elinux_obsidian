## *Definition*
- when pressing the keyboard to enter some characters it is stored somewhere called stream, and flow form this stream to the active program.
- **keyboard -> stream -> active program**
---
## *so what is a stream?*
* *[in languages]* means a continual flow of water from a point to another 
* *[in programming]* it represented as a source or destination of characters of infinite length 
* sequence of characters flowing 
* in the two points you do not know the quantity,
		فمكنش ينفع نقول نستخدم مثلا ال ارراي 
* **[finally]  you can say " it is an abstraction that represents a device on which input and output operations are performed " **
*  also streams are generally associated to a physical source or destination of characters, like a disk file, the keyboard, or the console so when performing any operation on streams, it is done on the associated device
```md
linux has 3 standard streams 

| name   | associated device | stream discriptor |
| ------ | ----------------- | ----------------- |
| input  | keyboard          | 0                 |
| output | screen            | 1                 |
| error  | screen            | 2                 |

```
---
فممكن نقول كدا ان هو المكان اللي بتخون فيه الدتا اللي انا مش عارف حجمها ايه ومنه بروح للبرنامج اللي شغال عليه 

# ==c++ how to handle streams==
### streams are handled in a header file _[library]_ called _[iostream]_ 
- so this is a dependency if using iostream
- next thing you identify function and obects
	- ### cin object form istream class
	- ### cout object from ostream class
	- and these object are declared in name space called ___std___
- we use insertion operator with cout <<
	- اكني بقوله خد الكلام ده واعرضه ليا في الاستريم اللي انا عاوزنه 
- and extraction operator with cin >> 
	- اكني بقوله هات الكلام من ال ستريم وحطة ليا ف ال مخزن ده

```cpp
#include <iostream>  // this ia a dependency
#include <string>
using namespace std;

//entry point

int main (void)
{
	string name;
	cout << "what's your name"<< endl;
	cin >> name;
	cout << "your name is: "<< name << endl;
	return 0;
}
```


![[1-templates.svg]]