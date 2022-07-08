https://archive.ph/Ckx54

# need solve


## Good String

https://leetcode.com/discuss/interview-question/2173518/Amazon-or-Good-String
图片

https://leetcode.com/discuss/interview-question/2174102/AMAZON-ONLINE-ASSESMENT/1447343



部分通过的答案

```java
def isDistinctRange(s: List[str], ranges: List[List[int]]) -> bool:
    for i in range(len(ranges)):
        l, r = ranges[i]
        s2 = []
        for j in range(l-1, r):
            if s[j] != '_':
                s2.append(s[j])
        if len(set(s2)) != len(s2):
            return False
    return True

def goodString(N: int, Q: int, S: str, arr: List[int], ranges: List[List[int]]) -> int:
    s = list(S)
    if isDistinctRange(s, ranges):
        return 0
    for i in range(len(arr)):
        s[arr[i] - 1] = '_'
        if isDistinctRange(s, ranges):
            return i + 1
```



##  Minimum swaps to sort an array
https://leetcode.com/discuss/interview-question/2149341/Amazon-OA

[2, 4, 3, 1, 6] -- 3 swaps
[3, 2, 1] -- 3 swaps
[4, 7] -- 0 swap
[7, 4] -- 1 swap

I tried a couple of approaches but could not pass most test cases. :(



 



## Minimum swaps to make the A Binary String Palindrome
https://leetcode.com/discuss/interview-question/2144970/Amazon-OA


https://logicmojo.com/minimum-swaps-to-make-palindrome


https://www.geeksforgeeks.org/minimum-count-of-bit-flips-required-to-make-a-binary-string-palindromic/



https://www.geeksforgeeks.org/count-minimum-swap-to-make-string-palindrome/



## Best combo (k most popular combos)

图片

sort 

https://leetcode.com/discuss/interview-question/2134960/Amazon-OA

https://leetcode.com/discuss/interview-question/1895396/amazon-sde-new-grad-oa-k-most-popular-combos


## Minimum money

https://leetcode.com/discuss/interview-question/2133434/AMAZON-OA


## Minnum diffenence

https://leetcode.com/discuss/interview-question/2132962/Amazon-OA

##  the number of second
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



## String palindrome
https://leetcode.com/discuss/interview-question/2068125/Amazon-or-OA-or-Seattle

Given a binary string write an algorithm to calculate minimum number of swaps required to make it a palindrome for eg 11101 requires on swap between 3rd and 4th to make it 11011




## Find the difference between task1 and task 2 

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



given an array consisting of only 1 and -1, return the max length of the subarray such that the product of all elements in said subarray is 1 https://leetcode.com/discuss/interview-question/1655441/amazon-oa








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



## Min number of swaps required to make binary string a palindrome
Range min query














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









 
 




## k most popular combos



https://leetcode.com/discuss/interview-question/1895396/Amazon-SDE-New-Grad-or-OA-or-k-most-popular-combos



https://leetcode.com/discuss/interview-question/1777410/Amazon-Online-Assesment-SDE-1/1272110

 



## .net stock price change minimum

第一题： aggregate temperature change evaluated on the ith day is the maximum of the sum of the changes in temperatures until the ith day, and the sum of the change in temperatures on the next (n - i) days, with the ith day temperature change included in both. Given the temperature data of n days, find the maximum aggregate temperature change



## minimum start health,游戏装甲伤害那一题

第二题：Given the stock [rices of n months, the net price change for the ith month is defined as the absolute difference between the average of stock prices for the first i months and for the remaining (n - i) months where 1 <= i /, n. Note that these averages are rounded down to an integer. Given an array of stock prices, find the month at which the net price change is minimum. If there are several such months, return the realiest month.







# 已解决

## 1. [Solved] minimum days to deliver all the parcels

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

https://www.1point3acres.com/bbs/thread-898185-1-1.html




## 2. [Solved] Password strength == Leetcode 2662

Password strength determination - Given a password determine the strength of the password which is calculated by getting substrings in password and calculating strength based on number of unique characters in the substring and adding all the strength

https://leetcode.com/problems/total-appeal-of-a-string/

https://www.1point3acres.com/bbs/thread-901320-1-1.html

## 3. [Solved] Maximum Twin Sum of a Linked List

photo twin-sum

https://leetcode.com/problems/maximum-twin-sum-of-a-linked-list/



## 4. [Solved] closest X destinations

https://leetcode.com/discuss/interview-question/1777410/Amazon-Online-Assesment-SDE-1/1272110

 

Same question :    https://leetcode.com/problems/k-closest-points-to-origin/

My assessment was completed recently. I am sharing the questions asked. Please feel free to suggest the approach.
One thing more, not only you have to solve coding problems, but also, you need to explain the approach and time complexity on a seperate notepad.

```
**PLEASE UPVOTE IF YOU FIND IT USEFUL.**



Here we go with the question:
**Question : 1**
Given a list of N possible delivery destinations, implement an algorithm to create the delivery plan for the closest X destinations.



**Input**
The input to the function/method consisits of two arguments:
*allLocations*, a list where each element consists of a pair of integers representing the x and y coordinates of the delivery locations;
*numDeliveries*, an integer representing the number of deliveries that will be delivered in the plan(X).



**Output**
Return a list of elements where each element of the list represents the X closest x and y integer coordinates of the delivery destinations, where X represents the *numDeliveries* input. If there is one tie, use the location with the closest X coordinate. If no location is possible, return a list with an empty location - not just an empty list.



**Constraints**
*numDeliveries*<=*size(allLocations)*



**Note**
The plan starts with the truck's location [0.0]. The distance of the truck from a delivery destination (x,y) is the square root of x^2 + y^2. If there are multiple ties, then return the locations starting with the closest X-coordinate as long as you satisfy returning exactly X delivery locations. The returned output can be in any order.



**Example
Input**
*allLocations* = [ [1,2], [3,4], [1,-1]]
*numDeliveries* = 2



**Output**
[ [1,-1], [1,2]]



**Explaination**
The distance of the truck from loaction [1,2] is square root(5) = 2.236.
The distance of the truck from loaction [3,4] is square root(25) = 5.
The distance of the truck from loaction [1,-1] is square root(2) = 1.414.



*numDeliveries* is 2, hence the output is [1,-1] and [1,2].

```

**Question 2:** https://leetcode.com/discuss/interview-question/1777426/Amazon-Online-Assessment-(follow-up)



## 5. [Solved] Server Power [Find Maximum Sustainable Cluster Size]

Net power consumption = maximum booting power among the k processors + (sum of processing power of processors)*k.
A cluster is said to be sustainable if it's net power consumption does not exceed a given threshold value powerMax.

Example:
bootingPower = [3,6,1,3,4]
processingPower = [2,1,3,4,5]
powerMax = 25

If k = 2, any adjacent pair can be choosen. The highest usage is the pair [4,5] with net power consumption 4 + (4 + 5)2 = 22. Next, try k = 3. Group the first 3 processors together as:
Here,
Max booting power = max(3,6,1)
Sum of processing power = 2 + 1+ 3 = 6
Net power consumption = 6 + 63 = 24 <= powerMax

Thus, k = 3 is a sustainable cluster.
Example:
bootingPower = [8,8,10,9,2]
processingPower = [4,1,4,5,3]
powerMax = 33

If k = 2, consisting of first 2 processors.
Net power consumption = max(8,8) + (4+1)*2 = 18 <= 33 (powerMax)

Thus, k = 2 is a sustainable cluster.

Example:
bootingPower = [11,12,19]
processingPower = [10,8,7]
powerMax = 6

k = 0, not possible to form any sustainable clusters.



## 6. [Solved] 2272. Substring With Largest Variance

https://leetcode.com/problems/substring-with-largest-variance/



max de‍‌‌‍‌‍viation among all substrings

https://www.1point3acres.com/bbs/thread-899236-1-1.html



## 7. [Solved] Economy Mart

```
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

```

 

## 8. [Solved] K Closest Points to Origin

https://leetcode.com/discuss/interview-question/2092307/Amazon-OA

: used a max heap (~nlogk solution) and passed all test cases (although using quickselect would've yielded a better time complexity on average but I don't think it's much of a big deal as long as it's not the naive approach w/ sorting the entire array. No need to take a risk when doing an interview unless required)



## 9. [Solved] Amazon warehouse load imbalance [ the number of segments]

given an array and an integer k, return the number of subarrays such that the difference between its max value and its min values is no more than k https://leetcode.com/discuss/interview-question/1904966/Amazon-orOAorset-7



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



Solution :   https://leetcode.com/discuss/interview-question/1994481/need-help-amazon-oa



## 10. [Solved] item rating

answer: https://leetcode.com/discuss/interview-question/1639758/amazon-oa-usa


https://www.1point3acres.com/bbs/thread-885897-1-1.html
https://www.1point3acres.com/bbs/thread-899236-1-1.html

rating
Subarrays





## [Solved]  the minimum number of swaps required so that the maximum element is at the beginning and the minimum element is at last
The first question was posted with a lot of other text, but ultimately you can boil it down to this :
Given N number of elements, find the minimum number of swaps required so that the maximum element is at the beginning and the minimum element is at last with the condition that only swapping of adjacent elements is allowed.
Examples:

Input: a[] = {3, 1, 5, 3, 5, 5, 2}
Output: 6
Step 1: Swap 5 with 1 to make the array as {3, 5, 1, 3, 5, 5, 2}
Step 2: Swap 5 with 3 to make the array as {5, 3, 1, 3, 5, 5, 2}
Step 3: Swap 1 with 3 at its right to make the array as {5, 3, 3, 1, 5, 5, 2}
Step 4: Swap 1 with 5 at its right to make the array as {5, 3, 3, 5, 1, 5, 2}
Step 5: Swap 1 with 5 at its right to make the array as {5, 3, 3, 5, 5, 1, 2}
Step 6: Swap 1 with 2 at its right to make the array as {5, 3, 3, 5, 5, 2, 1}
After performing 6 swapping operations 5 is at the beginning and 1 at the end
Input: a[] = {5, 6, 1, 3}
Output: 2
```
Find the index of the largest element(let l).
Find the index of the leftmost largest element if the largest element appears in the array more than once. Similarly, find the index of the rightmost smallest element(let r).
There exists two cases to solve this problem after this :
Case 1: If l < r: (Maximum is to the right of minimum element) Number of swaps = l + (n-r-1)
Case 2: If l > r: (Maximum is to the left of minimum element) Number of swaps = l + (n-r-2), as one swap has already been performed while swapping the larger element to the front.
```
```java
void solve(int a[], int n)
{
    int maxx = -1, minn = a[0], l = 0, r = 0;
    for (int i = 0; i < n; i++) {
 
        // Index of leftmost largest element
        if (a[i] > maxx) {
            maxx = a[i];
            l = i;
        }
 
        // Index of rightmost smallest element
        if (a[i] <= minn) {
            minn = a[i];
            r = i;
        }
    }
    if (r < l)
        cout << l + (n - r - 2);
    else
        cout << l + (n - r - 1);
}
```


## [Solved] Minimun Processing time

https://leetcode.com/discuss/interview-question/2239893/Amazon-OA-july-2022

**评论区答案**





## [Solved] 5. Get Heaviest Package

第一题Get Heaviest Package, 给一个int array 叫 package，如果package < package[i+1]，可以把i并到i+1里，反过来不行，求合并完之后最大的包裹

题目 ； https://leetcode.com/discuss/interview-question/1845746/Amazon-OA-or-March-2022-or-Questions

**评论区答案**

 
 ## [Solved] 6. findMaxProducts  从里面单调递增拿包裹

第二题也是package, 给一个int array, 从里面单调递增拿包裹，可以只拿一部分，例子是[7, 4, 5]取[3, 4, 5] ，也是求最大
两题思路都是一样的从后往前遍历，第一题O(N)，第二题O(N^2)
要用long不然会overflow

```
https://leetcode.com/discuss/interview-question/2108095/amazon-sde2-may-2022-online-&#8205;&#8205;&#8205;&#8204;&#8204;&#8205;&#8204;&#8205;&#8204;&#8205;&#8204;&#8205;&#8204;&#8205;&#8204;&#8204;&#8204;&#8204;&#8205;&#8204;assessment

```



## [Solved]  n piles of products （Array Strictly Increasing Order）
题目
https://leetcode.com/discuss/interview-question/2068122/Amazonor-OA

There are a total of n piles of products.
The number of products in each pile is represented by the array nums.
Select any subarray from the array nums and pick up products from that subarray such that the number of the products you pick from the ith pile is strictly less the than the number of the products you pick from the (i+1)th pile for all the indices i of the subarray.



Example
nums [7,4,5,2,6,5]
Choose subarray from indices (1,3) and pick products [3,4,5] respectively from each index, which is 12 products. Note that we are not forced to pick only 3 products from the index 1 as the maximum number of the products we can pick from index 2 is 4 and we need to make sure it is greater than the number of the products picked from index 1.



indices (3,6) [1,2,4,5] = 12
indices (3,5) = [1,26] = 9
indices (1,1) = 7



答案：

https://leetcode.com/discuss/interview-question/1988635/amazon-phone-screen-array-strictly-increasing-order




```java
public long findMaxProducts(List<Integer> products) {
        int l = products.size();
        long max = 0;
        for(int i=l-1;i>=0;--i) {
            if(i!=l-1 && products.get(i) < products.get(i+1)) continue;
            long localMax = products.get(i);
            long prev = localMax;
            for(int j=i-1;j>=0;--j) {
                prev = Math.min(prev-1, products.get(j));
                localMax+=prev;
                if(prev==1) break;
            }
            max = Math.max(localMax,max);
        }
        return max;
  }

```



# From Leetcode Discussion

## [Solved] maximize the median sum
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





## [Solved] sum-of-total-strength-of-wizards [Leetcode 2281]
2281. Sum of Total Strength of Wizards

定义Power[l, r] = (min power[i]) * ∑ power[i] where 'i' is from 'l' to 'r'
求sum of all power[i] mod 1000000007
example: [2, 3, 2, 1] 答案是 69:
power[0, 0] = 2 * 2 = 4;
power[0,1] = 2 *5 = 10;
power[0,2] = 2*7=14;
power[0,3] = 1*8=8;
...
power[3,3] = 1*1=1;


## [Solved] Cloudfront Caching

https://leetcode.com/discuss/interview-question/1144843/amazon-oa-april-2021-storage-optimization-cloudfront-caching


## [Solved] getHeaviest

```JAVA
public static int getHeaviest(int[] input) {
    int max = 0;
    for (int i = input.length - 1; i >= 0; --i) {
        if (input[i] < max) {
            max += input[i]; // merge
        } else {
            max = input[i]; // too big to merge - this is the new max
        }
    }
    return max;
}

```
 

## [Solved] Find Minimum Distance to Destination in a Grid
: a classic bfs problem. Doing a bfs while keeping track of the distance for each path yields the min distance to the destination point since bfs traverses all the connected paths from the starting point at the same time. Passed all test cases.

Got a follow-up from my recruiter about the on-site quite fast (no delay at all). Will post more about the interview experience after the on-site.

Update: got an offer! currently interviewing for other companies but probably will just take this one.




##  [solved] to be greater than K

题目 https://leetcode.com/discuss/interview-question/2072252/amazon

Find the minimum operations to be performed on the array to have maximum element in the sliding window of 3 to be greater than K. The only allowed operation would be to increase the element by 1.
Example :
Input : array = [1, 3, 0, 3, 1] , K=5
Output: 4
Explanation : Increasing the element at index (0-based Index) 1 and 3 two times.
**评论区答案**
https://leetcode.com/discuss/interview-question/2072252/amazon



## [solved] Find the minimum number that can be XOR-ed to each element in the given sorted array to arrange the array to be sorted in descending order

题目  https://leetcode.com/discuss/interview-question/2072252/amazon

Input : [2, 2, 4, 5]
Output : 5
Explanation : If each element is XOR-ed with 5, will yield the following array : [7, 7, 3, 0]

Could someone please help with the approach ?
**评论区答案**
https://leetcode.com/discuss/interview-question/2072252/Amazon





## obstacle robot
Determine the min distance required for the robot to remove the obstacle
Input is given as a 2D array which consists of 0, 1 and 9
9 is the obstacle, can pass through 1 and cannot pass through 0
Robot can move top, left, right and bottom

Input: [[1,0,0],[1,0,0],[1,9,1]]
output: 3





**默认只有一个obstacle**



BFS

类似参考： 1293. Shortest Path in a Grid with Obstacles Elimination


```
Write an algorithm to determine the minimum distance required for the demolition robot to remove the obstacle.



**Assumptions**
The demolition robot must start from the top-left corner of the lot, which is always *flat*, and can move one block up, down, left, or right at a time.
The demolition robot cannot enter *trenches* and cannot leave the *lot*.
The *flat areas* are represented as 1, areas with *trenches* are represented as 0 and the *obstacle* is represented by 9.



**Input**
The input to yhe function/method consists of one argument:
*lot*, representing the two-dimensional grid of integers;



**Output**
Return an integer representing the minimum distance traversed to remove the *obstacle* **else return -1**.



**Constraints**
1<=*rows,columns*<=10^3



**Example**
**Input**
*lot* = [ [1,0,0] , [1,0,0] , [1,9,1] ]



**Output**
3



**Explaination**
Starting from the top-left corner, the demolition robot traversed the cells (0,0) -> (1,0) ->(2,0) ->(2,1). The robot traversed the total distance 3 to remove the obstacle.
So, the output is 3.



```




# 题集

https://www.1point3acres.com/bbs/thread-699232-1-1.html



https://www.1point3acres.com/bbs/thread-715940-2-1.html
