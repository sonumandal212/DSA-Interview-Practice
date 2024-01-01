# [Check Armstrong](https://www.codingninjas.com/studio/problems/check-armstrong_589?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

## Problem statement
You are given an integer 'n'.
Return 'true' if 'n' is an Armstrong number, and 'false' otherwise.
Note:
An Armstrong number is a number (with 'k' digits) such that the sum of its digits raised to 'kth' power is equal to the number itself. For example, 371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371.
Example:
Input: 'n' = 1634
Output: true
Explanation:
1634 is an Armstrong number, as 1^4 + 6^4 + 3^4 + 4^4 = 1634
Detailed explanation ( Input/output format, Notes, Images )
Sample Input 1 :
1
Sample Output 1 :
true
Explanation of Sample Input 1 :
1 is an Armstrong number as, 1^1 = 1.
Sample Input 2 :
103
Sample Output 2 :
false
Expected Time Complexity:
Try to solve this in O(log(n)). 
Constraints:
1 <= ‘n’ <= 10^9
Time Limit: 1 sec


## Code

```cpp
#include<bits/stdc++.h>
bool checkArmstrong(int n){
	//Write your code here
	int temp = n;
	vector<int> ans;

	while(temp>0){
		int digit = temp % 10 ;
		ans.emplace_back(digit);
		temp /= 10;
	}

	int m = ans.size();
	int sum = 0;

	for(int i = 0 ; i < m ; i++){
		sum += pow(ans[i],m);
	}

	return sum == n;

}

```
## Time Complexity & Space Complexity
- Time complexity: O(log10(n))
- Space Complexity : O(log10(n))