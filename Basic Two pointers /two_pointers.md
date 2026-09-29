# Two Pointers 

Instead of using nested loops (O(n²)) , we can maintain two indices which coordinate with each other through an array or subarray to give O(n) instead of O(n²)

### Opposite direction pointers :

##### eg - Pair sum in sorted array 

```cpp
bool PairSum(vector<int> &nums , int x){
    int l = 0 , r = nums.size()-1 , sum ;

    while(l<r){
        sum = nums[l]+nums[r] ;
        if(sum == x){
            cout << nums[l] << " " << nums[r] ;
            return true ; 
        }else if(sum > x){
            r-- ;
        }else{
            l++;
        }
    }
    return false ;
}
```
