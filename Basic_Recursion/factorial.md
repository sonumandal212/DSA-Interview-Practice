# Factorial of a Number
## Problem Statement: 
Given a number X,  print its factorial.
To obtain the factorial of a number, it has to be multiplied by all the whole numbers preceding it. More precisely X! = X*(X-1)*(X-2) … 1.
Note: X  is always a positive number. 
Examples:
Example 1:
Input: X = 5
Output: 120
Explanation: 5! = 5*4*3*2*1
Example 2:
Input: X = 3
Output: 6
Explanation: 3!=3*2*1

## CODE
```cpp
#include <iostream>

using namespace std;

long long int fact(long long int n){
    long long int temp;
    if(n<0)
        return -1;
    if(n == 0 || n == 1)
        return 1;
    temp = fact(n-1)*n;
    return temp;
}

int main()
{
long long int n;
cin>>n;
cout<<fact(n)<<endl;
return 0;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(x)
- Space Complexity : O(x)