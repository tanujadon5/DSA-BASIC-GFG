```cpp
vector<int> minAnd2ndMin(int a[], int n) {
    vector<int> v;
    int min1 = INT_MAX;
    int min2 = INT_MAX;
    for(int i = 0; i<n; i++){
        if(a[i] < min1 && a[i] < min2){// jab a[i] min1 & min2 dono se chota h
            min2 = min1;
            min1 = a[i]; // min1 m a[i] ki value assign hogi
        }
        else if(a[i] < min2 && a[i] != min1){ // jab a[i] bss min2 se chota h
        //a[i] should not be equal to min1
            min2 = a[i]; // min2 m a[i] ki value assign hogi
        } 
    }
    if(min2 == INT_MAX){ // min2 is not updated, all elements are same in array
        v.push_back(-1);
    }
    v.push_back(min1);
    v.push_back(min2);
    return v;
    
}
```
