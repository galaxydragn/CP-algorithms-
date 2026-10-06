# Bitwise

### There are 6 bitwise operators : 

1. AND (&) : 1 if both bits are 1
2. OR ( | ) : 1 if either bit is 1
3. NOT (~) : ~1 = 0 and ~0 = 1
4. XOR(^) : 1 if bits differ
5. Left Shift (<<) : a<<k means a*(2^k)
6. Right Shift (>>) : a>>k means a/(2^k)

### XOR properties :
1. a ^ a = 0
2. a ^ 0 = a
3. a ^ b = b ^ a (commutative and associative)
4. If a ^ b = c, then a ^ c = b

### Common Tricks :

1. Is n odd ?
```cpp  
if(n^1 == 0){
  cout << "odd" ;
}else{
  cout << "even" ;
}
```

2. Multiply/Divide by 2
multiply : n << 1
divide : n >> 1

3. To find 2^k :
   if k <= 30    then use 1<<k
   else if 31<=k<=62 then use 1LL<<k

4. To check if kth bit is 1 : 
   ```cpp
   ((n>>k)&1)
   ```
  
