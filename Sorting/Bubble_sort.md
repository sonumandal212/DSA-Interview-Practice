# [Bubble Sort](https://www.youtube.com/watch?v=HGk_ypEuS24)

- Push the maximum no to the last by doing adjecent swaping.

```cpp
#include<bits/stdc++.h>
using namespace std;

void bubble_sort(int n, int arr[]){
    for(int i = n-1 ;i>0 ;i--){
        for(int j = 0 ; j<=i-1 ;j++){
            if(arr[j]>arr[j+1])
                swap(arr[j],arr[j+1]);
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
    
    bubble_sort(n,arr);
    
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