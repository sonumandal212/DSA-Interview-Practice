# [Count Digits](https://www.codingninjas.com/studio/problems/count-digits_8416387?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)

## Problem statement
You are given a number ’n’.
Find the number of digits of ‘n’ that evenly divide ‘n’.

Note:
A digit evenly divides ‘n’ if it leaves no remainder when dividing ‘n’.

Example:
Input: ‘n’ = 336
Output: 3

Explanation:
336 is divisible by both ‘3’ and ‘6’. Since ‘3’ occurs twice it is counted two times.
Note:
You don’t need to print anything. Just implement the given function.

Detailed explanation 
Sample Input 1:
35
Sample Output 1:
1
Explanation of sample output 1:
35 is only divisible by ‘5’, hence answer is 1.

Sample Input 2:
373
Sample Output 2:
0

Explanation of sample output 2:
There’s no digit in 373 that evenly divides it. Hence the output is 0.
Expected Time Complexity:
Try to solve this in O(log(n)) 

Constraints:
1 <= ‘n’ <= 10^9
Time Limit: 1 sec

## CODE
```cpp
    int countDigits(int n){
	// Write your code here.
	int count =0;
	int temp = n;


	while(n>0){
		int digit = n % 10;
		
		if(digit != 0 && temp % digit == 0)
			count++;
		n /= 10;
	}
	return count;	
}

```

## Time complexity & Space Complexity
- Time complexity: O(log n)
- Space complexity: O(1)



# [Number of digits](https://www.codingninjas.com/studio/problems/number-of-digits_9173?utm_source=youtube&utm_medium=affiliate&utm_campaign=striver_Arrayproblems&leftPanelTabValue=PROBLEM)

## Problem statement
You are given a number 'n'.
Return number of digits in ‘n’.
Example:
Input: 'n' = 123
Output: 3
Explanation:
The 3 digits in ‘123’ are 1, 2 and 3. 

Detailed explanation ( Input/output format, Notes, Images )
Sample Input 1:
121
Sample Output 1:
3
Explanation of sample output 1:
There are 3 digits in 121 are 1,2 and 1.
Sample Input 2:
38
Sample Output 2:
2
Expected time complexity :
The expected time complexity is O(log n).
Constraints:
1 <= ‘n’ <= 10^9

- We can use (log10()+1) for counting the number of digits present in the number. ex: log10(7789) = 3.81... so, we can use (int)log10(7789)+1 = 4
## CODE
```cpp
#include<bits/stdc++.h>
int countDigits(int n){
	// Write your code here.
	return ((int)log10(n)+1);	
}
```

## Time complexity & Space Complexity
- Time complexity: O(log n)
- Space complexity: O(1)