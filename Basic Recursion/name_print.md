# Print Name N times using Recursion

## CODE
```cpp
#include <bits/stdc++.h>
using namespace std;

void name(int n){
    if(n==0)
        return;
    cout<<"Sourish"<<endl;
    name(n-1);
}
int main(){
    int n;
    cin>>n;
    name(n);

return 0 ;
}
```
## time complexity and space complexity
- time complexity: O(n)
- space complexity : O(n)