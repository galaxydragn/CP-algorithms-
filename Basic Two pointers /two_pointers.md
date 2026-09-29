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

##### eg - Sum of three integers equal to 0

```cpp
void tripletsum(vector<int> &nums){
    sort(nums.begin() , nums.end()) ;
    int n = nums.size() ;
    for(int i = 0 ; i < n-2 ; i++){
        if(i>0 && nums[i] == nums[i-1])continue ;
        int l = i+1 ;
        int r = n-1 ;
        while(l<r){
            int sum = nums[l] + nums[r] + nums[i] ;
            if(sum == 0){
                cout << nums[i] << " " << nums[l] << " " << nums[r] ;
                l++ ; r-- ; 
                while(l<r && nums[l] == nums[l-1])l++ ;
                while(l<r && nums[r] == nums [r+1])r-- ;
            }else if (sum < 0){
                l++ ;
            }else{
                r-- ;
            }
        }
    }
}
```

