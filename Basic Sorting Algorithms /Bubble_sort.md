# Bubble sort

<img width="300" height="400" alt="WhatsApp Image 2026-09-23 at 10 57 20" src="https://github.com/user-attachments/assets/c939f153-da2b-44fd-9b40-52bdb88126f2" />

<br><br>


```cpp
vector<int> bubble_sort(vector<int> &nums){
    int n = nums.size() ;
    for(int i = 0 ; i < n-1 ; i++){
        bool swapped = false ;
        for(int j = 0 ; j < n-i-1 ; j++){
            if(nums[j] > nums[j+1]){
                swap(nums[j] , nums[j+1]);
                swapped = true ;
            }
        }
        if(!swapped){
            break ;
        }
    }
    return nums ;
}
```

