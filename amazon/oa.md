https://archive.ph/Ckx54

# from 1 points
## minimum days to deliver all the parcels

There is N delivery centers. Each Devliery Outlet has some packages to be delivered, denoted by parcels[i]. There is a Rule how delivery should be completed. On each day, an equal number of parcerls are to be dispatched from each delivery center that has atleast one parcel remaining.

Find minimum nunmber of days needed to deliver all the parcels.
Input:
parcels= {2,3,4,3,3}

Output
3

Solutions:
Iterate over the list/ array, count distinct elements i.e desired minimum days

Please post if you know any other logic/ soultions.




https://www.1point3acres.com/bbs/thread-898185-1-1.html






## 2262
https://www.1point3acres.com/bbs/thread-901320-1-1.html







## max de‍‌‌‍‌‍viation among all substrings
https://www.1point3acres.com/bbs/thread-899236-1-1.html




## item rating
https://www.1point3acres.com/bbs/thread-885897-1-1.html
https://www.1point3acres.com/bbs/thread-899236-1-1.html

rating
Subarrays




## Get Heaviest Package

第一题Get Heaviest Package, 给一个int array 叫 package，如果package < package[i+1]，可以把i并到i+1里，反过来不行，求合并完之后最大的包裹

第二题也是package, 给一个int array, 从里面单调递增拿包裹，可以只拿一部分，例子是[7, 4, 5]取[3, 4, 5] ，也是求‍‌





# From Leetcode Discussion

## maximize the median sum
https://leetcode.com/discuss/interview-question/1565781/Amazon-or-OA-or-maximize-the-median-sum/1142854

Given an array of integers (unsorted) and a value n indicating number of channels. You have to send all these numbers through n channels (At least one number should go through each channel)
Ex: 1 2 3 2 1 5 , n=3
Send 1 2 3 using channel 1, 2 using channel 2, 1 5 using channel 3.
Calculate median of each channel :
channel 1 , median of (1 2 3) is 2
channel 2, median of (2) is 2
channel 3, median of (1 5) is 3
sum = 7

1 2 3 2 1 5 , n=3
Send 1 2 2 1 using channel 1, 3 using channel 2, 5 using channel 3.
Calculate median of each channel :
channel 1 , median of (1 2 2 1) is 1.5
channel 2, median of (3) is 3
channel 3, median of (5) is 5
sum = 9.5

In case someone has across this question and my understanding differs, do let me know.



```
Sort the array in decreasing order. Assign top n-1 values to n-1 channels. Median of all these will be their value only. Remaining must be sent through last channel. Calculate the median of these elements and then output the sum.
```




## GOod String

https://leetcode.com/discuss/interview-question/2173518/Amazon-or-Good-String
图片



##  Minimum swaps to sort an array
https://leetcode.com/discuss/interview-question/2149341/Amazon-OA

[2, 4, 3, 1, 6] -- 3 swaps
[3, 2, 1] -- 3 swaps
[4, 7] -- 0 swap
[7, 4] -- 1 swap

I tried a couple of approaches but could not pass most test cases. :(






## segment subarray  与上面类似
 Amazon warehouse has a group of n items of various weights lined up in a row. A segment of contiguously placed items can be shipped ogether if only if the difference betweeen the weihts of the heaviest and lightest item differs by at most k to avoid load imbalance.

Given the weights of the n items and an integer k, fine the number of segments of items that can be shipped together.

Note: A segment (l,r) is a subarray starting at index l and ending at index r where l less than equal(<=) r.

Example:
weights = [1, 3, 6], k=3

weight difference between max and min for each (l,r) index pair are:

(0,0) -> max(weights[0]) - min(weights[0]) = max(1)-min(1) = 1-1 =0
(0,1) - > max(weights[0],weights[1]) - min(weights[0],weights[1])= max(1,3)-min(1,3)=3-1=2
(0,2) - > max(weights[0],weights[1],weights[2]) - min(weights[0],weights[1],weights[2])= max(1,3,6)-min(1,3,6)=6-1=5
(1,1) -> max(weights[1]) - min(weights[1]) = max(3)-min(3) = 3-3 =0
(1,2) -> max(weights[1],weights[2]) - min(weights[1],weights[2]) = max(3,6)-min(3,6) = 6-3 =3
(2,2) -> max(weights[2])-min(weights[2]) = max(6)-min(6) = 6-6 =0

as only 5 out 6 pair, is less than equal equal to k (3) , so the number of segments that can shipped together is 5.

Constraints
-- 1<=k, weights[i] <=10^9
-- 1 <= n <=3*10^5



## Minimum swaps to make the A Binary String Palindrome
https://leetcode.com/discuss/interview-question/2144970/Amazon-OA


https://logicmojo.com/minimum-swaps-to-make-palindrome


https://www.geeksforgeeks.org/minimum-count-of-bit-flips-required-to-make-a-binary-string-palindromic/



https://www.geeksforgeeks.org/count-minimum-swap-to-make-string-palindrome/

## get the password strength 

2262
, same as https://leetcode.com/problems/total-appeal-of-a-string/



## Best combo

图片


sort

https://leetcode.com/discuss/interview-question/2134960/Amazon-OA

https://leetcode.com/discuss/interview-question/1895396/amazon-sde-new-grad-oa-k-most-popular-combos


## MInmum money

https://leetcode.com/discuss/interview-question/2133434/AMAZON-OA


## Minnum diffenence

https://leetcode.com/discuss/interview-question/2132962/Amazon-OA


## 
https://leetcode.com/discuss/interview-question/2131732/Amazon-OA

Parade in HackerLand
The people in HackerLand, are getting ready for a parade, and the participants are all mixed up. There should be no instance where a red uniform is immediately to the left of a blue one.
Given a binary string, 0 denotes a person in red uniform and 1 denotes a person in blue uniform. The goal is to remove any occurrence of "01" in the binary string. More formally, at each second, all the substrings "01 "in the string s are changed to "10". This process repeats until no "0/11 is present in the string. All the substrings "01" in the current state of sare changed at the same time.
Find the number of seconds it takes for this process to stop.
Example color = "001011"
Here is a simulation of the process where t denotes the current time. t= 0, color = "001011" t= 1, color = "010101" t= 2, color = "101010" t= 3, color = "110100" t= 4, color = "111000"
0101->1010->1100 ans:2

Hence this process takes 4 seconds.



## Prefix Sum 

Appeared for Amazon OA recently, for internship role. This was the question
Given an Array contaning N integers find the prefix of the M times.
Example N=3
M=2
arr= 1 2 3
O/P-> 1 4 10
N=5
M=3
Arr= 1 2 3 4 5
O/P= 1 5 15 35 70
While converting to prefix sums, do the operation modulo 10^9 +7.
1<=N<=1000
1<=M,arr[i]<=10^9

I could pass only half the TCs. Remaning Time Limit Exceeding. how to solve it



## Array Strictly Increasing Order

https://leetcode.com/discuss/interview-question/1988635/Amazon-or-Phone-Screen-or-Array-Strictly-Increasing-Order
There are a total of n piles of products.
The number of products in each pile is represented by the array nums.
Select any subarray from the array nums and pick up products from that subarray such that the number of the products you pick from the ith pile is strictly less the than the number of the products you pick from the (i+1)th pile for all the indices i of the subarray.

Example
nums [7,4,5,2,6,5]
Choose subarray from indices (1,3) and pick products [3,4,5] respectively from each index, which is 12 products. Note that we are not forced to pick only 3 products from the index 1 as the maximum number of the products we can pick from index 2 is 4 and we need to make sure it is greater than the number of the products picked from index 1.

indices (3,6) [1,2,4,5] = 12
indices (3,5) = [1,26] = 9
indices (1,1) = 7


also

https://leetcode.com/discuss/interview-question/2068122/Amazonor-OA

## K Closest Points to Origin
https://leetcode.com/discuss/interview-question/2092307/Amazon-OA

: used a max heap (~nlogk solution) and passed all test cases (although using quickselect would've yielded a better time complexity on average but I don't think it's much of a big deal as long as it's not the naive approach w/ sorting the entire array. No need to take a risk when doing an interview unless required)



## Find Minimum Distance to Destination in a Grid
: a classic bfs problem. Doing a bfs while keeping track of the distance for each path yields the min distance to the destination point since bfs traverses all the connected paths from the starting point at the same time. Passed all test cases.

Got a follow-up from my recruiter about the on-site quite fast (no delay at all). Will post more about the interview experience after the on-site.

Update: got an offer! currently interviewing for other companies but probably will just take this one.
