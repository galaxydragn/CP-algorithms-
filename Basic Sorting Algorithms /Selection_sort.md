# Selection Sort

<img width="1087" height="1600" alt="WhatsApp Image 2026-09-23 at 16 11 28" src="https://github.com/user-attachments/assets/d305d387-919c-4cf1-b99e-065c1cd88571" />

<br><br>

### Algorithm

```cpp
vector<int> selection_sort(vector<int> &nums){
    int n = nums.size() ;
    for(int i = 0 ; i < n - 1 ; i ++){
        int minidx = i ;
        for(int j = i+1 ; j < n ; j ++){
            if(nums[j] < nums[minidx]){
                minidx = j ; 
            }
        }
        swap(nums[i] , nums[minidx]) ;
    }
    return nums ;
}
```

#### NOTE :
1.Time complexity : O(n²)
