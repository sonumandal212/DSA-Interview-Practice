# [Selection Sort](https://www.youtube.com/watch?v=HGk_ypEuS24)

- Select minimum and swap 

## Aproach
Lets consider the following array as an example: arr[] = {64, 25, 12, 22, 11}

### 1. First pass:

  - For the first position in the sorted array, the whole array is traversed from index 0 to 4 sequentially. The first position where 64 is stored presently, after traversing whole array it is clear that 11 is the lowest value.
  - Thus, replace 64 with 11. After one iteration 11, which happens to be the least value in the array, tends to appear in the first position of the sorted list.

![Selection Sort Algorithm | Swapping 1st element with the minimum in array](https://media.geeksforgeeks.org/wp-content/uploads/20230524115038/1.webp)

### 1. Second Pass:

  - For the second position, where 25 is present, again traverse the rest of the array in a sequential manner.
  - After traversing, we found that 12 is the second lowest value in the array and it should appear at the second place in the array, thus swap these values.

![Selection Sort Algorithm | swapping i=1 with the next minimum element](https://media.geeksforgeeks.org/wp-content/uploads/20230526165135/2.webp)

- 1. Third Pass:

 - Now, for third place, where 25 is present again traverse the rest of the array and find the third least value present in the array.
 - While traversing, 22 came out to be the third least value and it should appear at the third place in the array, thus swap 22 with element present at third position.

![Selection Sort Algorithm | swapping i=2 with the next minimum element](https://media.geeksforgeeks.org/wp-content/uploads/20230526165200/3.webp)

### 1. Fourth pass:

  - Similarly, for fourth position traverse the rest of the array and find the fourth least element in the array 
  - As 25 is the 4th lowest value hence, it will place at the fourth position.

![Selection Sort Algorithm | swapping i=3 with the next minimum element](https://media.geeksforgeeks.org/wp-content/uploads/20230526165244/4.webp)

### 1. Fifth Pass:

 - At last the largest value present in the array automatically get placed at the last position in the array
 - The resulted array is the sorted array.

![Selection Sort Algorithm | Required sorted array](https://media.geeksforgeeks.org/wp-content/uploads/20230526165320/5.webp)


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