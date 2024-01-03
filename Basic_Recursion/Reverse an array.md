# Reverse a given Array
## Problem Statement: 
You are given an array. The task is to reverse the array and print it. 
Examples:
Example 1:
Input: N = 5, arr[] = {5,4,3,2,1}
Output: {1,2,3,4,5}
Explanation: Since the order of elements gets reversed the first element will occupy the fifth position, the second element occupies the fourth position and so on.
Example 2:
Input: N=6 arr[] = {10,20,30,40}
Output: {40,30,20,10}
Explanation: Since the order of elements gets reversed the first element will occupy the fifth position, the second element occupies the fourth position and so on.

## Space-optimized iterative method

```cpp
#include <bits/stdc++.h>

using namespace std;


void reverse_array(int arr[],int n){
    int p1=0,p2=n-1;
    for(int i = 0;i<n/2;i++){
        swap(arr[p1],arr[p2]);
        p1++;
        p2--;
    }
    for(int i = 0;i<n;i++){
        cout<<arr[i]<<" ";
    }
}
int main()
{
    int n;
    cin >> n;
    int arr[n];
    for(int i=0;i<n;i++) 
        cin >> arr[i];
    reverse_array(arr,n);
    
return 0;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)


## Recursive method


```cpp
#include <bits/stdc++.h>
using namespace std;
void reverse_array(int arr[],int n,int start,int end){
    if(start<end){
        swap(arr[start],arr[end]);
        reverse_array(arr,n,start+1,end-1);
    }
}
int main()
{
    int n;
    cin >> n;
    int arr[n];
    for(int i=0;i<n;i++) 
        cin >> arr[i];
    reverse_array(arr,n,0,n-1);
    for(int i=0;i<n;i++) 
        cout << arr[i] << " ";
    
return 0;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)