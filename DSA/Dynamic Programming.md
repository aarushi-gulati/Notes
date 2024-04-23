## **Initial concept making**
Suppose you have a very big problem P. You don't know how to solve P but you know you could divide it into several sub-problems P1, P2, P3... . You could also further divide them until we arrive to a sub-problem that could be trivially solved. 

e.g.:- In order to find the sum of all the elements of an array {big problem - P}, we divide the array into smaller parts {P1, P2, P3..} and keep on dividing until we reach a sub-array with a single element jiska sum we know would be the element itself. 

> Break a problem into smaller sub-problems -> Know how to get answer for bigger problem from smaller sub-problems -> What is the smallest sub-problem which is trivial to solve -> What is the biggest sub-problem - known as the base-case. 

**Now where does Dynamic Programming come up in the above statement?**
> While dividing the problem into smaller subproblems, are there some repetitions that are happening?

==Memoization==: Storing the results of calculation in some place, to be used later. 
The two steps involved are:- 
1. Check if this subproblem has been solved before. 
2. Update/retrieve the value. 

## e.g.:- The case of fibonacci numbers. 

![[Pasted image 20240103184207.png]]
Here
* f(2) and f(1) are trivial cases.
* f(3) and f(4) are repeated cases. 

> To store the results, we have the choice of either using a map or an array to store the results -  if the key values are integers, the better choice is to use an array because a map may use order of n in the worst case.  

## How to solve a dp problem?
1. Think about a sub-problem (state). You should be aware of the parameter - the thing that uniquely separates a sub-problem from others. 
2. Think about breaking it into smaller sub-problems. 
3. Think about the relation between smaller sub-problems to compute bigger sub-problem. (Transition)
4. Where does the above relation not work (base case).
5. What is the biggest problem to solve (final sub-problem). 

Recursive approach aka top down approach - generally slower since they require stack space. 
Iterative approach aka bottom up approach. 

## Time and space complexity 
Tight bound time complexity -> O(transition time) = summation of all transition times
Loose bound time complexity -> O(No. of states * avg transition time per state)

## Where can we apply dp?
1. Number of ways
2. Min/max answer 
3. Checking for possibility 

> DP can be looked at as an optimized brute force OR identifying overlapping sub-problems. 

---
## Dice Combinations 
https://cses.fi/problemset/task/1633
==My understanding of the approach==: For any n, there could be 6 inputs - and for each input, there could further be 6 sub-inputs. 
We stop input-ing once our sum variable reaches >= n -> equal to me increase the count and greater than me go to the last iteration without increasing the count. 

Using DP -> f(n) = f(n - 1) + f(n - 2) + f(n - 3) + f(n - 4) + f(n - 5) + f(n - 6)
where dp[k] = number of ways to get a sum of k 

and each of these could be further divided. 
Trivial cases -> 0, 1 lie the answer would be 1. 

4 -> 1 + 1 + 1 + 1, 1 + 1 + 2, 1 + 2 + 1, 1 + 3, 2 + 2, 2 + 1 + 1, 3 + 1, 4

Initial approach:
```
import sys
sys.setrecursionlimit(10**9)
MOD = 1000000007

def f(n):
	if n < 0:
	return 0
	if dp[n] != -1:
		return dp[n]
	dp[n] = (f(n - 1) + f(n - 2) + f(n - 3) + f(n - 4) + f(n - 5) + f(n - 6)) % MOD
	return dp[n]

n = int(input())
dp = [-1] * (n + 1)
dp[1] = 1
dp[0] = 1

result = f(n)
print(result)
```
Above code gave runtime error for large values of n. 
So apparently, fuck python. 

```
#include <bits/stdc++.h>
using namespace std;

int main(){
	int n;
	cin>>n;
	vector <int> dp(n + 1);
	dp[0] = 1;
	for(int i = 1; i <= n; i++){
		for (int j = 1; j <= 6; j++){
			if (j <= i){
				dp[i] = (dp[i] + dp[i - j]) % 1000000007;
			}
		}
	}
	cout<<dp[n]<<endl;
}
```

---
## Minimising coins
https://cses.fi/problemset/task/1634
==My understanding of the approach==:- For every i among the n coins, dp[x] is the ~~number of ways we could get the sum x.~~ minimum number of coins required to get sum x.

```
#include <bits/stdc++.h>
using namespace std;

int main(){
	int n, x;
	cin>>n>>x;
	vector <int> dp(x + 1, INT_MAX - 1);
	vector<int> coins(n);
	
	for(int i = 0; i <n; i++){
		cin>>coins[i];
	}
	
	dp[0] = 0;
	
	for(int i = 1; i <= x; i++){
		for (int j = 0; j < n; j++){
			if (coins[j] <= i){
				dp[i] = min(dp[i], 1 + dp[i - coins[j]]);
			}
		}
	}
	
	if (dp[x] == 2147483646){
		cout<<-1;
	}
	
	else{
		cout<<dp[x];
	}
}
```

---
## Coin Combinations I
https://cses.fi/problemset/task/1635
==My understanding of the approach==: 
State: dp[i] will represent the number of ways in which a given number could be represented in. 
Base case: dp[0] = 1
Transition: dp[i] = summation for all j in coins(dp[i - j])
Very similar to the dice problem. 

```
#include <bits/stdc++.h>
using namespace std;

int main(){
	int n, x;
	cin>>n>>x;
	vector <int> dp(x + 1, 0);
	vector<int> coins(n);
	
	for(int i = 0; i <n; i++){
		cin>>coins[i];
	}
	
	dp[0] = 1;
	
	for(int i = 1; i <= x; i++){
		for (int j = 0; j < n; j++){
			if (coins[j] <= i){
				dp[i] = (dp[i] + dp[i - coins[j]]) % 1000000007;
			}
		}
	}
	cout<<dp[x];
}
```

