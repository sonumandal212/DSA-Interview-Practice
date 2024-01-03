# Check if the given String is Palindrome or not

## Problem Statement: 
“Given a string, check if the string is palindrome or not.”  A string is said to be palindrome if the reverse of the string is the same as the string.
Examples:
Example 1:
Input: Str =  “ABCDCBA”
Output: Palindrome
Explanation: String when reversed is the same as string.
Example 2:
Input: Str = “TAKE U FORWARD”
Output: Not Palindrome
Explanation: String when reversed is not the same as string.


## using reverse function 

```cpp
#include <bits/stdc++.h>
using namespace std;

void check_palin(string s){
    string temp = s;
    reverse(temp.begin(),temp.end());
    if(s == temp)
        cout<<"Palindrome"<<endl;
    else cout<<"Not Palindrome"<<endl;   
}
int main()
{
string s;
getline(cin,s);
check_palin(s);
return 0;
}
```
## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)

## using recursion

```cpp
#include <bits/stdc++.h>
using namespace std;

bool check_palin(int i,string &s){
    if(i>=s.size()/2)
        return true;
    if(s[i] != s[s.size()-i-1])
        return false;
    return check_palin(i+1,s);
}

int main()
{
string s;
getline(cin,s);
bool flag = check_palin(0,s);

if (flag == true)
    cout<<"Palindrome"<<endl;
else cout<<"Not Palindrome"<<endl;

return 0;
}

```

## Time Complexity & Space Complexity
- Time Complexity : O(n)
- Space Complexity : O(n)