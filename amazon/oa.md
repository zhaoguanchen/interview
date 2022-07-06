https://archive.ph/Ckx54

# from 1 points
## minimum days to deliver all the parcels
Keyword:parcels,deliver


There is N delivery centers. Each Devliery Outlet has some packages to be delivered, denoted by parcels[i]. There is a Rule how delivery should be completed. On each day, an equal number of parcerls are to be dispatched from each delivery center that has atleast one parcel remaining.

Find minimum nunmber of days needed to deliver all the parcels.
Input:
parcels= {2,3,4,3,3}

Output
3

Solutions:
Iterate over the list/ array, count distinct elements i.e desired minimum days

Please post if you know any other logic/ soultions.


Solution
```java
class Solution {
  public int maxArea(int[] parcels) {
        Set<Integer> seen = new HashSet<>();
        
        for(int num : parcels) {
            if(0 == num) {
                continue;
            }
            
            seen.add(num);
        }
        
        return seen.size();
    }
}
```



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

## array
Find the minimum operations to be performed on the array to have maximum element in the sliding window of 3 to be greater than K. The only allowed operation would be to increase the element by 1.
Example :
Input : array = [1, 3, 0, 3, 1] , K=5
Output: 4
Explanation : Increasing the element at index (0-based Index) 1 and 3 two times.

Find the minimum number that can be XOR-ed to each element in the given sorted array to arrange the array to be sorted in descending order
Input : [2, 2, 4, 5]
Output : 5
Explanation : If each element is XOR-ed with 5, will yield the following array : [7, 7, 3, 0]

Could someone please help with the approach ?

https://leetcode.com/discuss/interview-question/2072252/Amazon

## String palindrome
https://leetcode.com/discuss/interview-question/2068125/Amazon-or-OA-or-Seattle

Given a binary string write an algorithm to calculate minimum number of swaps required to make it a palindrome for eg 11101 requires on swap between 3rd and 4th to make it 11011


## Password strength
Password strength determination - Given a password determine the strength of the password which is calculated by getting substrings in password and calculating strength based on number of unique characters in the substring and adding all the strength


##  n piles of products
图片
https://leetcode.com/discuss/interview-question/2068122/Amazonor-OA



## Demolition robot
Determine the min distance required for the robot to remove the obstacle
Input is given as a 2D array which consists of 0, 1 and 9
9 is the obstacle, can pass through 1 and cannot pass through 0
Robot can move top, left, right and bottom

Input: [[1,0,0],[1,0,0],[1,9,1]]
output: 3


## Minimum Days to Deliver All Parcels
https://leetcode.com/discuss/interview-question/1998840/Amazonor-OA-or-Minimum-Days-to-Deliver-All-Parcels 

There is N delivery centers. Each Devliery Outlet has some packages to be delivered, denoted by parcels[i]. There is a Rule how delivery should be completed. On each day, an equal number of parcerls are to be dispatched from each delivery center that has atleast one parcel remaining.

Find minimum nunmber of days needed to deliver all the parcels.
Input:
parcels= {2,3,4,3,3}

Output
3

Solutions:
Iterate over the list/ array, count distinct elements i.e desired minimum days

Please post if you know any other logic/ soultions.


## Find Maximum Sustainable Cluster Size

https://leetcode.com/discuss/interview-question/1636493/Amazon-or-OA-or-Max-Length-of-Valid-Server-Cluster

Question2:
Give you a list servers. Their processing power is given as a array of integer, and boot power as a array of integer.
Write a function to return the max length of sub array which's power consumption is less than or equal to max power limit.
Formula to calculate the power consumption for a subArray is:
Max(bootPower[i...j]) + Sum(processPower[i....j]) * length of subArray.

Note: Single server is also a subArray, return 0 if no such subArray can be found.

public int MaxLengthValidSubArray(int[] processingPower, int[] bootingPower, int maxPower)
{}
Does anyone know what is the similar question in leetcode?



## nnn

https://leetcode.com/discuss/interview-question/2023674/Amazon-OA
Given an array consisting of N integer and two number k,d.
Task1-From the given array we can choose k consecutive elements one after in array and after that leave an array element.Then we calculate maximum sum of all such consecutive element containing subarray.
Task2-From the given array we can choose k+d consecutive elements one after in array and after that leave an array element.Then we calculate maximum sum of all such consecutive element containing subarray.
Find the difference between task1 and task 2 ans.
ex 1->arr=[1,2,3,4,8,9,10]
k=2,d=1;
Task1 elements {3,4}+{9,10}=7+19=26
Task2 elements {1,2,3}+{8,9,10}=6+27=33;
output=33-26=7



## the maximum subarray length with a product of 1.


A question about Amazon student badges but ultimately the problem was given an arr of -1 or 1, return the maximum subarray length with a product of 1.
The array is of size 2 and above and only contains -1 and 1
e.g arr = [-1,-1,1,1,-1], return 4, since index 0 to 3 have the max length with product equal to 1

I tried to use a sliding window but only passed 4/13 cases. there was somthing i had to fix in the logic for the case arr = [ -1,-1,-1,-1,-1, 1]




Given an array containing only 0 and 1 as its elements. We have to sort the array in such a manner that all the ones are grouped together and all the zeros are grouped together. The group of ones can be either at the start of the array or at the end of the array. The constraint while sorting is that every one/zero can be swapped only with its adjacent zero/one. Find the minimum number of moves to sort the array as per the description.
Example:
input array ={0,1,0,1}
Final array = {0,0,1,1}
Minimum moves = 1 (1 at index 1 is swapped with 0 at index 2)

input array = { 1101}
Final array - {1110}
Minimum moves = 1 {1 at index 2 is swapped with index 3}

I passed all test cases on this one 13/13.

I ran a sliding window to check number of swaps if the elements on the left should be 0s before 1s, and at each 0 found by right index, I found the number of swaps needed
repeated the same above for the case if the elements on the left should be 1s before 0s,
returned the minimum of both operations.

Do I have even a miniscule chance of moving forward



## Min no. of swaps required to make binary string a palindrome
Range min query







## Maximum Twin Sum of a Linked List
photo twin-sum

https://leetcode.com/problems/maximum-twin-sum-of-a-linked-list/





given an array consisting of only 1 and -1, return the max length of the subarray such that the product of all elements in said subarray is 1 https://leetcode.com/discuss/interview-question/1655441/amazon-oa
given an array and an integer k, return the number of subarrays such that the difference between its max value and its min values is no more than k https://leetcode.com/discuss/interview-question/1904966/Amazon-orOAorset-7






## restaurant orders
roblem statement
You are the owner of a restaurant. On a particular day, there are N orders coming in. The billing policy for each order is as follows:

For each minute of preparation of the order, the cost is K units of money.
For each minute when an order has been received, but its preparation has not been started, W units of money is discounted.
The chef in the restaurant believes that it is most profitable if he follows the following rules to select the sequence in which he prepares the orders:

If no order is being prepared, start preparing the order that has the least preparation time from among the pending orders.
If there are two or more pending orders having the same preparation time, pick the order that was received first.
If the waiting discount is greater than the cost of preparation, the order is considered to be free which means, money earned is 0.
Task
Determine the money earned for the completion of each order.

Assumptions

N = 4
K = 5
W = 1
each-order has [x,y] where x is the start time of the order and y is the preparation of the order.
Example:
orders = [[1,4],[2,2],[3,3],[9,1]]
Output -> [20,7,13,5] -
[1,4] (1 is the start time,4 is the processing time)-> 20
As its a first job and no need to wait. and the cost would be is * 5-1 * 0(4 is the processing time taken,5 is the cost for every processing minute,1 is the cost for every wait minute,0 as its not waiting for any order)
[2,2]-> 7 as it needs to wait till 5sec(1+4) -> 5 * 2-3 * 1
[3,3] 13 as it needs to wait till 5sec(1+4)-> 5 * 3-2 * 1
[9,1] 5 no need to wait -> 5 * 1-0

This will be solved using priority queues based on the completion time.
but how to solve the use-case of "If no order is being prepared, start preparing the order that has the least preparation time from among the pending orders."



## Economy Mart


Economy Mart is a very popular e-commerce platform because they display the cheapest items first. Economy Mart has decided to migrate its database to Amazon's cloud platform. The product listings in the old database are being migrated into the Amazon database. Customers that go onto Amazon.com will be viewing items from the new database.

Economy Mart has an unusual way of displaying items,

If a customer views the first item, they will be shown the cheapest item in the database

If a customer is currently viewing the kth cheapest item, viewing the next item will display the (k+1)th cheapest item.

If multiple items have the same price, they are ordered alphabetically ascending.

There are 2 types of entries:

The first element in the row is “INSERT” followed by the name of the item (String) and its price (String denoting an Integer). This describes an item being added to the database.

The first element in the row is the word “VIEW”. This is when the customer views an item. The other 2 elements in these rows contain "-" that can be ignored. It is guaranteed that at least one item is added to the database when a customer views an item.

Table of entries
image

Note: The price of each item is in string format so you may need to convert it to an integer before using it.

While the database is being transferred, an unknowing customer logs onto the website and browses some of Economy Mart's items. Given a server log in chronological order, determine which items were shown to the customer.

Example

entries = [['INSERT', 'milk', '4'], ['INSERT', 'coffee', '3'], ['VIEW', '-', '-'], ['INSERT', 'pizza', '5'], ['INSERT', 'gum', '1'], ['VIEW', '-', '-']]

Let's consider the following entries in the database:

INSERT milk 4
INSERT coffee 3
VIEW - -
INSERT pizza 5
INSERT gum 1
VIEW - -

In this case, milk and coffee are added to the database at costs of 4 and 3, respectively. When the customer logs onto the site, the cheapest item in the database is shown: coffee.

image

While the customer is browsing, pizza and gum are added to the database. Pizza is worth 5 and gum is worth 1. When the customer views the next cheapest item, the items in the database in sorted order are gum (1), coffee (3), milk (4), and pizza (5). Since the customer is viewing for the second time, the second cheapest item, coffee, will be shown again.

image

Return ['coffee', 'coffee'].

Function Description

Complete the function getItems in the editor below.

getItems has the following parameters:

string entries[n][3]: each row in the matrix represents an individual log entry

Returns

string[]: answers to each of the "VIEW" queries

Constraints

1 ≤ n ≤ 105
1 ≤ | itemName | ≤ 10 (The name of each item will be 1 to 10 characters long)

Item names will only consist of lowercase English letters.

All itemName strings are distinct

1 ≤ price ≤ 109

k ≤ length of the database (That is, there will always be at least k items in the database when the customer is viewing for the kth time)

Input Format For Custom Testing

The first line of input contains n, the number of entries in the log.

The second line contains the number 3, the size of each entry.

The following n lines each contain an entry with 3 space-separated values.

Sample Case 0

Sample Input For Custom Testing

STDIN FUNCTION

10 → entries[][] size n = 10
3 → entries[n][] columns = 3
INSERT fries 4 → rows of entries
INSERT soda 2
VIEW - -
VIEW - -
INSERT hamburger 5
VIEW - -
INSERT nuggets 4
INSERT cookie 1
VIEW - -
VIEW - -

Sample Output

soda
fries
hamburger
nuggets
hamburger

Explanation

Add 'fries' for 4. db = ['fries'] (costs = [4])
Add 'soda' for 2. db = ['soda', 'fries'] (costs = [2, 4])

For the first "VIEW", the cheapest item in the database, soda, is shown.

For the second "VIEW", the second cheapest item in the database, fries, is shown.

Add 'hamburger' for 5. db = ['soda', 'fries', 'hamburger'] (costs = [2, 4, 5])

For the third 'VIEW", the third cheapest item is shown: hamburger.

Add 'nuggets' for 4, the same price as 'fries'. Sort nuggets and fries alphabetically. db = ['soda', 'fries', 'nuggets', 'hamburger'] ( costs = [2, 4, 4, 5])

Add 'cookie' for 1. db = ['cookie', 'soda', 'fries', 'nuggets', 'hamburger'] ( costs = [1, 2, 4, 4, 5])

For the fourth "VIEW", the fourth cheapest item is nuggets.

For the fifth "VIEW", the fifth cheapest item is hamburger.

Sample Case 1

Sample Input For Custom Testing

STDIN FUNCTION

9 → entries[][] size n = 9
3 → entries[n][] columns = 3
INSERT ruler 4 → rows of entries
VIEW - -
INSERT notecards 2
VIEW - -
INSERT notebook 9
INSERT backpack 10
INSERT pens 6
INSERT pencils 5
VIEW - -

Sample Output

ruler
ruler
pencils

Explanation

First, ruler, worth 4, is added to the database. The database contains ruler = 4.

Next, the customer views the database for the first time. The cheapest item in the database is ruler.

notecards is added to the database and is worth 2. The database contains notecards = 2 and ruler = 4.

The customer decides to view the next cheapest item. After the first item, he is shown the second cheapest item in the database, ruler.

notebook is added to the database and is worth 9. The database contains notecards = 2, ruler = 4, and notebook = 9.

backpack is added to the database and is worth 10. The database contains notecards = 2, ruler = 4, notebook = 9, and backpack = 10.

pens is added to the database and is worth 6. The database contains notecards = 2, ruler = 4, pens = 6, notebook = 9, and backpack = 10.

pencils is added to the database and is worth 5. The database contains notecards = 2, ruler = 4, pencils = 5, pens = 6, notebook = 9, and backpack = 10.

For the third and last viewing, the third cheapest item is pencils.

## 2272

https://leetcode.com/problems/substring-with-largest-variance/



## 1438

1. Amazom warehouse 相关的题 是 lc药思散罢 的变种



1438.  	Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit









## Economy Mart

1. 2.Economy Mart 相关的题 lc  饵以岭饵变种‍‌‌&







## Minimum swaps to sort an array





## Amazon warehouse load imbalance

```
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
```

# 题集

https://www.1point3acres.com/bbs/thread-699232-1-1.html



https://www.1point3acres.com/bbs/thread-715940-2-1.html
