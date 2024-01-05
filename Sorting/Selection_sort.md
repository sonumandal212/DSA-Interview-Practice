# Selection Sort



## CODE

```cpp
#include<bits/stdc++.h>
using namespace std;

void selection_sort(int n, int arr[]){
    for(int i = 0;i<=n-2;i++){
        int mini = i;
        for(int j = i ; j<=n-1 ;j++){
            if(arr[j]<arr[mini])
                mini = j;
        }
        swap(arr[i],arr[mini]);
    }
}

int main(){
    int n;
    cin>>n;
    
    int arr[n];
    for(int i = 0; i<n ; i++){
        cin>> arr[i];
    }
    
    selection_sort(n,arr);
    
    for(int i = 0;i<n;i++)
        cout<<arr[i]<<" ";

    return 0;
}

```
## Time Complexity & Space Complexity
- Best, Avg and Wrost TC : O(n^2)
- Space Complexity : O(1)