## Dutch National Flag/3-Way Quicksort
An array arr[l....r] is divided into 3 parts:
* arr[l...i] elements less than pivot. 
* arr[i + 1...j - 1] elements equal to pivot. 
* arr[j...r] elements greater than pivot.

## Find all elements that appear more than "n/k" times
Ek approach of above could be to use hashing to have O(N) and O(N)  complexity. But we could use Moore's Voting algorithm to have O(N) and O(1) complexities. 

## Moore's Voting Algorithm
As there can be at max **k – 1** elements present in the array which appears more than **n/k** times so their will be **k – 1** candidates. When we encounter an element which is one of our candidates then increment the count else decrement the count.
* We declare a temp array that stores candidate elements and their respective counts. 
* We traverse through the given array and modify the temp array(add/remove elements and increase/decrease their respective counts).
* Iterate through the final k - 1 elements and check if their count actually is more than n/k.

## Kadane's Algorithm
* We carry subarray till it given positive sum. 
* The subarray with negative sum is discarded(by assigning currentSum = 0).

To implement the maximum contiguous subarray sum problem using DP, we:
For each index i, DP[i] stores the maximum possible Largest Sum Contiguous Subarray ending at index i, and therefore we can calculate DP[i] using the mentioned state transition:
- DP[i] = max(DP[i-1] + arr[i] , arr[i] )

## Rearrange array in alternating positive and negative items with O(1) extra space 
* The idea is to find the first element that is out of place - a positive element at odd index or a negative one at an even index. 
* Find the immediate next element with opposite sign. 
* Right rotate the array elements between the two elements. 

## Factorial of large number 
* Initialise an array result = [None] * 500 and size = 1.
* Initialise value stored in result as 1. 
* Multiply numbers from 2 to n and store the results in result. 
* Multiplication is carried out as:- 
	- Initialise carry =  0 
	- Find value of result[i] * x + carry. Let this be equal to prod. 
	- Update result[i] by storing the last digit of prod in it. 
	- Update carry by storing the remaining digits in carry. 
- Put all digits of carry in result and increase size by the number of digits in carry. 

```
def multiply(i, result, size):
    carry = 0
    x = 0
    while(x < size):
        prod = result[x] * i + carry
        result[x] = prod % 10
        carry = prod // 10
        x += 1
    while(carry):
        result[size] = carry % 10
        carry = carry // 10 
        size += 1
    return size
    
class Solution:
    def factorial(self, N):
        result = [0] * 500000
        result[0] = 1
        size = 1
        i = 2
        while(i <= N):
            # print(size)
            size = multiply(i, result, size)
            i += 1
        required = result[:size]
        return required[::-1]
```

