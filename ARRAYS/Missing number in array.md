```cpp
class Solution{
  public:
    int MissingNumber(vector<int>& array, int n) {
        // IMPLEMENT  A.P. in range 1 to n qs
        int missing_no,array_sum;
        int total_sum =(n*(n+1))/2;
        for(int i = 0; i<n-1; i++){
            array_sum += array[i];
        }
        missing_no = total_sum - array_sum;
        return missing_no;
    }
};
```
