We use frequency arrays and hashmap to count the occurrences of the elements.

If the values are small non-negative integers and the range is known then its preferable to use frequency arrays 

```cpp
int arr[] = {1, 3, 2, 3, 1, 1, 4};
int n = 7;

int freq[100005] = {0}; // zero-initialized, size = max possible value + 1

for (int i = 0; i < n; i++) {
    freq[arr[i]]++;
}

// freq[1] = 3, freq[2] = 1, freq[3] = 2, freq[4] = 1
for (int i = 1; i <= 4; i++) {
    cout << i << " -> " << freq[i] << "\n";
}
```
##### Counting characters :

```cpp
string s = "banana";
int freq[26] = {0};

for (char c : s) {
    freq[c - 'a']++;   // maps 'a'->0, 'b'->1, ..., 'z'->25
}
```


for (int i = 0; i < 26; i++) {
    if (freq[i] > 0) {
        cout << char('a' + i) << " -> " << freq[i] << "\n";
    }
}
// a -> 3, b -> 1, n -> 2
```
