This allows us to calculate the sum of the elements of any range of an array in O(1) instead of O(n) 

```cpp
vector<int> a(n+1) , prefixsum(n+1,0) ;
for(int i = 1 ; i < n+1 ; i ++)
  cin >> a[i] ;
for(int i = 1 ; i < n+1 ; i ++){
  prefixsum[i] = prefixsum[i-1]+a[i] ;
```
Now , prefixsum[i] is nothing but summation of a[1 .... i]

Sum of the elements from a[i] to a[j] is actually prefixsum[j]-prefixsum[i]

