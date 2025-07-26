  
**DAY 1**  
[1295\. Find Numbers with Even Number of Digits](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)

Link: [https://leetcode.com/problems/find-numbers-with-even-number-of-digits/description/](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/description/)

Example :  
**Input:** nums \= \[12,345,2,6,7896\]  
**Output:** 2

| Approach 1: Math Division Method Count digits by dividing the number by 10 repeatedly TC: O(n × log₁₀(max number)) | Approach 2: String Conversion Convert the number to string and check the length   TC: O(n)  | Approach 3: Math.log10() Method Use logarithmic formula to count digits: `digits = floor(log₁₀(num)) + 1 `   TC : O(n)  |
| :---- | :---- | :---- |
| **Initialize even \= 0 for each number in nums:     Convert number to string     if length of string % 2 \== 0:         even \= even \+ 1 Return even** | **for each number in nums:     Set count \= 0     WHILE number \> 0:      number \= number / 10         count \= count \+ 1     IF count % 2 \== 0:         even \= even \+ 1 Return even**  | **Initialize even \= 0 FOR each number in nums:     IF number \== 0:         digits \= 1     ELSE:         digits \= floor(log10(number)) \+ 1     IF digits % 2 \== 0: even \= even \+ 1**  |

**DAY 1**  
**TWO SUM**  
Link :[https://leetcode.com/problems/two-sum/description/](https://leetcode.com/problems/two-sum/description/)

Example  
**Input:** nums \= \[2,7,11,15\], target \= 9  
**Output:** \[0,1\]  
**Explanation:** Because nums\[0\] \+ nums\[1\] \== 9, we return \[0, 1\].

Approach:

| Brute Force | Optimal  |
| :---- | :---- |
| Time Complexity: O(n2) | Time Complexity: O(n2) |
| Traverse through each element and check the addition \== target | Use hash Map |
|     public int\[\] twoSum(int\[\] nums, int target){         for(int i \= 0 ; i\<nums.length ; i++){             for (int j \= i+1 ; j\<nums.length ; j++){                 if(nums\[i\]+nums\[j\] \== target){                     return new int\[\] {i,j};                 }             }         }         return new int\[0\];  |     public int\[\] twoSum(int\[\] nums, int target) {         Map\<Integer, Integer\> map \= new HashMap\<\>();         for (int i \= 0; i \< nums.length; i++) {             int diff \= target \- nums\[i\];             if (map.containsKey(diff))                 return new int\[\] { map.get(diff), i };             map.put(nums\[i\], i);         }         return new int\[0\];  |

DAY 2 : FIZZ BUZZ(Easy)  
Link: [https://leetcode.com/problems/fizz-buzz/description/](https://leetcode.com/problems/fizz-buzz/description/)

Example:  
Answer\[i\] \== “FizzBuzz’’ if i is div by 3 & 5  
Answer\[i\] \== “Fizz’’ if i is div by 3   
Answer\[i\] \== “Buzz’’ if i is div by 5  
Answer\[i\] \== i (as a string)  if none is true

Input: n=5  
Output: \[“1” , “2” , “Fizz” , “4” , “Buzz”\]

| Pseudo Code |  Code |
| :---- | :---- |
| /\* take input int n create an arraylist \= result traverse i from 1 to n if i%3 \== 0 && i%5 \== 0 add FizzBuzz in result elseif i%3 \== 0 add Fizz in result elseif i%5 \== 0 add Buzz in result else add i(String) in result print result \*/  TC: O(n) SC:O(n) |     public static List\<String\> fizzBuzz(int n) {         List\<String\> result \= new ArrayList\<\>();         for(int i \= 1; i \<= n; i++){             if(i%3\==0 && i%5\==0){                 result.add("FizzBuzz");             }             else if (i%3 \== 0){                 result.add("Fizz");             }             else if(i%5 \== 0){                 result.add("Buzz");             }             else{                 result.add(Integer.toString(i));             }         }         return result ;  |

DAY 2: Remove Linked List Elements(Hard)  
Link:[https://leetcode.com/problems/remove-linked-list-elements/](https://leetcode.com/problems/remove-linked-list-elements/)

Example:  
Input: head \= \[1,2,6,3,4,5,6\], val \= 6  
Output: \[1,2,3,4,5\]

Input: head \= \[7,7,7,7\], val \= 7  
Output: \[\]

Code:  
