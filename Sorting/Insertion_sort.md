# [Insertion Sort](https://www.youtube.com/watch?v=HGk_ypEuS24)

- Always take an element and place it in its correct order.


```cpp
#include<bits/stdc++.h>
using namespace std;

void insertion_sort(int n, int arr[]){
    for(int i = 0 ;i<n;i++){
        int j = i;
        while(j>0 && arr[j-1]>arr[j]){
            swap(arr[j],arr[j-1]);
            j--;
        }
    }
}

int main(){
    int n;
    cin>>n;
    
    int arr[n];
    for(int i = 0; i<n ; i++){
        cin>> arr[i];
    }
    
    insertion_sort(n,arr);
    
    for(int i = 0;i<n;i++)
        cout<<arr[i]<<" ";
    cout<<endl;

    return 0;
}

```
## Time Complexity & Space Complexity
- Best case TC : O(n)
- Avg and Wrost TC : O(n^2)
- Space Complexity : O(1)