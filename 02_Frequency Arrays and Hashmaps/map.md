# map

map is actually a tree, not a hash table

### Basic Syntax and declaration :

```cpp
#include <map>
using namespace std ;
map<string,int> age ;

age["Ram"] = 23 ;
age["Sam"] = 26 ;
age["Ashok"] = 28 ;

for(auto& [name,year] : age){
  cout << name << "-->" << age ;
}
```
Output : 
```cpp
Ram-->23
Sam-->26
Ashok-->28
```
Output is ALWAYS alphabetically sorted by key
