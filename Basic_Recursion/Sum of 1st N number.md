# Sum of first N Natural Numbers
Problem statement: Given a number ‘N’, find out the sum of the first N natural numbers.
Examples:
Example 1:
Input: N=5
Output: 15
Explanation: 1+2+3+4+5=15
Example 2:
Input: N=6
Output: 21
Explanation: 1+2+3+4+5+6=15

## Code
```cpp
#include <bits/stdc++.h>
using namespace std;

void sum_of_N_number(int i,int n,int &sum){
    if(i==n+1){
        return ;
    }
    sum+=i;
    sum_of_N_number(i+1,n,sum);
}

int main(){
    int n;
    cin>>n;
    int sum=0;
    sum_of_N_number(1,n,sum);
return 0 ;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)


## or we can use this approach

```cpp
#include<bits/stdc++.h>
using namespace std;
void func(int i, int sum){
   // Base Condition.
   if(i<1)
   {
       cout<<sum<<endl;
       return;
   }
   // Function call to increment sum by i till i decrements to 1.
   func(i-1,sum+i);
}
int main(){ 
  // Here, let’s take the value of n to be 3.
  int n = 3;
  func(n,0);
  return 0;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)