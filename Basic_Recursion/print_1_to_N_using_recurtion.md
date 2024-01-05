# Print 1 to N using Recursion

## CODE

```cpp
#include <iostream>
using namespace std;

void print(int i,int n){
    if(i > n)
        return;
    cout<<i<<" ";
    print(i+1,n);
}

int main()
{
    int n;
    cin>>n;
    print(1,n);

    return 0;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)


# [1 to N Without Loop](https://www.codingninjas.com/studio/problems/print-1-to-n_628290?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)

## Problem statement
You are given an integer ‘n’.
Your task is to return an array containing integers from 1 to ‘n’ (in increasing order) without using loops.
Example:
Input: ‘n’ = 5
Output: 1 2 3 4 5
Explanation: An array containing integers from ‘1’ to ‘n’ is [1, 2, 3, 4, 5].
Detailed explanation ( Input/output format, Notes, Images )
Sample Input 1:
5
Sample Output 1 :
1 2 3 4 5
Explanation Of Sample Input 1:
The array contains all integers from 1 to 5 in ascending order.
Sample Input 2:
2
Sample Output 2:
1 2
Explanation Of Sample Input 2:
The array contains all integers from 1 to 2 in ascending order.
Expected Time Complexity:
The expected time complexity is O(n), where 'n' is the given integer.
Constraints:
1 <= n <= 10^6
Time Limit: 1-sec

## CODE
```cpp
vector<int> printNos(int x) {
    // Write Your Code Here
    if(x==0)
        return vector<int>();
     vector<int> ans = printNos(x-1);
     ans.emplace_back(x);
    return ans;
}
```

## Time Complexity & Space Complexity
- Time Complexity : O(x)
- Space Complexity : O(x)