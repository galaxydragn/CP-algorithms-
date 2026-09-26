Hashmaps stores values in key-value pair.

## Unordered_map

### Basic Syntax and declaration :

```cpp
#include <unordered_map>
using namespace std ;
unordered_map<string,int> age ;
```
Here in this unordered map , keys are string and their ages are taken as int 

### Ways to insert and update :
```cpp
age["Ram"] = 23 ;
age["Sam"] = 26 ;                          //This method of delcaration overwrites the value 

age.insert({"Ashok" , 28});                //It does not overwrite if key already exists 
age.insert(make_pair("Ravi" , 22));        //older style 

age["Ram"] = 29 ;                          //Now value of Ram is 29 which has overwritten the value 26
```
### NOTE :
If key does not exist then mp[key] creates it automatically with default value ie , 0 for int and "" for string 

```cpp
unordered_map<string,int> mp ;
cout << mp.size() ;
cout << mp["alok"];
cout << mp.size() ;
```

Output : 
```cpp
0
0
1
```

### Checking if a key exist :
```cpp
if(age.count("Ram")){
  cout << "Ram is in the map";
}
```
mp.cout(key) returns 1 if the key exists else 0

```cpp
if(age.find("Ram")!= age.end()){
  cout << "Found" ;
}
```
find() does the same thing and returns an iteration 


### Deleting key
```cpp
age.erase("Ravi") ;
```

### Iterating through unordered_map() :
```cpp
unordered_map<string, int> age = {{"Ram", 29}, {"Sam", 26}, {"Ashok", 28}};

// Modern way (C++17+) — structured bindings, very readable
for (auto& [name, years] : age) {
    cout << name << " is " << years << " years old\n";
}

// Older/equivalent way
for (auto& p : age) {
    cout << p.first << " is " << p.second << " years old\n";
    // p.first = key, p.second = value
}
```
