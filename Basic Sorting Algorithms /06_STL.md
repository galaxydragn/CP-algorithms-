We will be using 
```cpp
#include <algorithm>
```
most of the time for competitive programming.

##### Sorting an array :

```cpp
vector<int> v = {5, 2, 8, 1, 9};
sort(v.begin(), v.end());              // ascending: 1 2 5 8 9
sort(v.begin(), v.end(), greater<int>()); // descending: 9 8 5 2 1
```
##### Sort only part of the range:

```cpp
sort(v.begin(), v.begin() + 3); // sort first 3 elements only
```

##### Custom comparator (lambda):

```cpp
sort(v.begin(), v.end(), [](int a, int b) {
    return a > b; // descending
});
```

##### 
