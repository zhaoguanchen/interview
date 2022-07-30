some experience 
1point3acres.com/bbs/thread-801493-1-1.html
给定正整数n求0到n所有数字中024出现的次数之和10-->0出现2次2和4分别出现1次返回422-->0出现32出现64出现2返回112brokenkeyboard3messagesplit
https://www.1point3acres.com/bbs/thread-902780-1-1.html

# 高频

## 4*4 matrix

```
在几个4*4 matrix中各找一个missing element，marked by '?’，然后找到的element的大小给这些matrices排序，如果都一样则保持原顺序
```

```
给input一个matrix，这个matrix是很多个 4*4 的小matrix并排摆放。 （size 是4行，4*k 列）
每个4*4matrix里都应该是 1-16 这16个数字，但是每个matrix里都有一个是“？” missing。
需要把所有的“？”按照缺的数字填回去，然后根据他们填回去的数字的大小顺序 从左到右re-arrange这些matrix。
如果missing value一样，保持matrix的原顺序。
return 修改后的大 matrix
```



## list of queries

```
给定a，b，比如a=[1,2,3], b=[4,5]；同时给定一个list of queries，query有两种情况：（1）比如[0,1,x]，0就是a，1就是指a中的index为1，x指的是a[index] = x，这个操作不需要对res进行更新； (2）比如[1,m]，即输出a，b中相加等于m的所有情况的数量，比如m=5, 那么只有1+4符合情况，则res.append(1)。 值得一提的是这题对时间复杂度要求比较高
```

```

```





## same letter

```
给一个String Array strs[ ], return含3个及以上相同字母的string的个数
```

```
在一个类似于str="aaa bbb ccd"中数出重复字母超过三个的个数，比如现在就是aaa,bbb符合条件，所以return 2
```

```java
```



# 训练



# 一亩三分地



第一题：很简单所以忘了。。
第二题：在一个类似于str="aaa bbb ccd"中数出重复字母超过三个的个数，比如现在就是aaa,bbb符合条件，所以return 2
第三题：在几个4*4 matrix中各找一个missing element，marked by '?’，然后找到的element的大小给这些matrices排序，如果都一样则保持原顺序
第四题：给定a，b，比如a=[1,2,3], b=[4,5]；同时给定一个list of queries，query有两种情况：（1）比如[0,1,x]，0就是a，1就是指a中的index为1，x指的是a[index] = x，这个操作不需要对res进行更新； (2）比如[1,m]，即输出a，b中相加等于m的所有情况的数量，比如m=5, 那么只有1+4符合情况，则‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌res.append(1)。 值得一提的是这题对时间复杂度要求比较高
目前uber的oa应该很多在codesignal上面进行，推荐大家先做practise熟悉一下平台。


## 024

```
   给定正整数n，求0到n所有数字中0， 2， 4出现的次数之和
   10 --> 0出现2次，2和4分别出现1次，返回4
   22 --> 0出现3， 2出现6，4出现2，返回11
```

```java
public class Solution {
  public int sum(int n) {
    
  }
}
```

 一个城市有三个区域 A， B， C。 是从A到C的包含关系。（A是B的子区域，B是C的子区域）
给input三个list，是list of strings for 地铁站名。 另有input 两个string，是origin 和destination站名。
地铁票有三种，AB，  BC， ABC。价格按照这个顺序便宜到贵。
问给定的两站之间最便宜的地铁票是这三种的哪一种。如果站名不存在return “”。

## message slipt

```
给一个 String[ ][ ] str代表用户的聊天记录，width代表屏幕大小，userwidth代表聊天框大小
顶部和底部要width个“*”，左右补个“+”， 用户消息1靠左显示，2靠右显示，消息超过userwidth要开第新一行, 每一行都要用“ ”补全到width个，左右再补个“|”, return String[ ]显示每一行的字符
eg. str = [
["1", "Hello how r u"]
["2", "Good u"]
["1", "Good"]
],
width = 15, userwidth = 5
output = [
"+***********+"
"|Hello         |"
"|how r        |"
"|u               |"
"|        Good|"
"|               u|"
"|Good        |"
"+***********+"
]
```



## 



```
nput是 a list of strings。问有多少个 i， j 的 index pair，such that strings 是 strings[j] 的prefix。
return pair 个数
```









## broken keyboard



swap to make strictly increasing

```
You are given an array of non-negative integers numbers. You are allowed to choose any number from this array and swap any two digits in it. If after the swap operation the number contains leading zeros, they can be omitted and not considered (eg: 010 will be considered just 10).

Your task is to check whether it is possible to apply the swap operation at most once, so that the elements of the resulting array are strictly increasing.

Example

For numbers = [1, 5, 10, 20], the output should be makeIncreasing(numbers) = true.
The initial array is already strictly increasing, so no actions are required.

For numbers = [1, 3, 900, 10], the output should be makeIncreasing(numbers) = true.
By choosing numbers[2] = 900 and swapping its first and third digits, the resulting number 009 is considered to be just 9. So the updated array will look like [1, 3, 9, 10], which is strictly increasing.

For numbers = [13, 31, 30], the output should be makeIncreasing(numbers) = false.
The initial array elements are not increasing.
By swapping the digits of numbers[0] = 13, the array becomes [31, 31, 30] which is not strictly increasing;
By swapping the digits of numbers[1] = 31, the array becomes [13, 13, 30] which is not strictly increasing;
By swapping the digits of numbers[2] = 30, the array becomes [13, 31, 3] which is not strictly increasing;
So, it's not possible to obtain a strictly increasing array, and the answer is false.


```

2. Map

```
You've created a new programming language, and now you've decided to add hashmap support to it. Actually you are quite disappointed that in common programming languages it's impossible to add a number to all hashmap keys, or all its values. So you've decided to take matters into your own hands and implement your own hashmap in your new language that has the following operations:

insert x y - insert an object with key x and value y.
get x - return the value of an object with key x.
addToKey x - add x to all keys in map.
addToValue y - add y to all values in map.
To test out your new hashmap, you have a list of queries in the form of two arrays: queryTypes contains the names of the methods to be called (eg: insert, get, etc), and queries contains the arguments for those methods (the x and y values).

Your task is to implement this hashmap, apply the given queries, and to find the sum of all the results for get operations.

Example

For queryType = ["insert", "insert", "addToValue", "addToKey", "get"] and query = [[1, 2], [2, 3], [2], [1], [3]], the output should be solution(queryType, query) = 5.

The hashmap looks like this after each query:

1 query: {1: 2}
2 query: {1: 2, 2: 3}
3 query: {1: 4, 2: 5}
4 query: {2: 4, 3: 5}
5 query: answer is 5
The result of the last get query for 3 is 5 in the resulting hashmap.
```

3. Minesweeper

```
Minesweeper is a popular single-player computer game. The goal is to locate mines within a rectangular grid of cells. At the start of the game, all of the cells are concealed. On each turn, the player clicks on a blank cell to reveal its contents, leading to the following result:
If there's a mine on this cell, the player loses and the game is over;
Otherwise, a number appears on the cell, representing how many mines there are within the 8 neighbouring cells (up, down, left, right, and the 4 diagonal directions);
If the revealed number is 0, each of the 8 neighbouring cells are automatically revealed in the same way.
demonstration

You are given a boolean matrix field representing the distribution of bombs in the rectangular field. You are also given integers x and y, representing the coordinates of the player's first clicked cell - x represents the row index, and y represents the column index, both of which are 0-based.

Your task is to return an integer matrix of the same dimensions as field, representing the resulting field after applying this click. If a cell remains concealed, the corresponding element should have a value of -1.

It is guaranteed that the clicked cell does not contain a mine.

Example

For
field = [[false, true, true],
         [true, false, true],
         [false, false, true]]
x = 1, and y = 1, the output should be

solution(field, x, y) = [[-1, -1, -1],
                         [-1, 5, -1],
                         [-1, -1, -1]]
example

There are 5 neighbors of the cell (1, 1) which contain a mine, so the value in (1, 1) should become 5, and the other elements of the resulting matrix should be -1 since no other cell would be expanded.

For
field = [[true, false, true, true, false],
         [true, false, false, false, false],
         [false, false, false, false, false],
         [true, false, false, false, false]]
x = 3, and y = 2, the output should be

solution(field, x, y) = [[-1, -1, -1, -1, -1],
                         [-1, 3, 2, 2, 1],
                         [-1, 2, 0, 0, 0],
                         [-1, 1, 0, 0, 0]]
example

Since the value in the cell (3, 2) is 0, all of its neighboring cells ((2, 1), (2, 2), (2, 3), (3, 1), and (3, 3)) are also revealed. Since the value in the cell (2, 2) is also 0, its neighbouring cells (1, 1), (1, 2) and (1, 3) are revealed, and since the value in cell (2, 3) is 0, its neighbours (1, 4), (2, 4), and (3, 4) are also revealed. The cells (3, 3), (2, 4), and (3, 4) also contain the value 0, but since all of their neighbours have already been revealed, no further action is required.

Input/Output

[execution time limit] 3 seconds (java)

[input] array.array.boolean field

A rectangular matrix representing the locations of the mines in the game field.

Guaranteed constraints:
2 ≤ field.length ≤ 100,
2 ≤ field[i].length ≤ 100.

[input] integer x

The row number of the cell which is clicked (0-based).

Guaranteed constraints:
0 ≤ x < field.length.

[input] integer y

The column number of the cell which is clicked (0-based).

Guaranteed constraints:
 0 ≤ y < field[0].length.

[output] array.array.integer

The expanded matrix after the click.
```




4. 

```
You are given a string s. Consider the following algorithm applied to this string:

Take all the prefixes of the string, and choose the longest palindrome between them.
If this chosen prefix contains at least two characters, cut this prefix from s and go back to the first step with the updated string. Otherwise, end the algorithm with the current string s as a result.
Your task is to implement the above algorithm and return its result when applied to string s.

Note: you can click on the prefixes and palindrome words to see the definition of the terms if you're not familiar with them.

Example

For s = "aaacodedoc", the output should be solution(s) = "".

The initial string s = "aaacodedoc" contains only three prefixes which are also palindromes - "a", "aa", "aaa". The longest one between them is "aaa", so we cut if from s.
Now we have string "codedoc". It contains two prefixes which are also palindromes - "c" and "codedoc". The longest one between them is "codedoc", so we cut if from the current string and obtain the empty string.
Finally the algorithm ends on the empty string, so the answer is "".
For s = "codesignal", the output should be solution(s) = "codesignal".
The initial string s = "codesignal" contains the only prefix, which is also palindrome - "c". This prefix is the longest, but doesn't contain two characters, so the algorithm ends with string "codesignal" as a result.

For s = "", the output should be solution(s) = "".
```









```
Given two arrays a and b and list of queries. Return the values of all (1) query in an array.
Queries are of two types:
(0) update [type, index of element in a, value]. Update the element in a by given value
(1) get [type, sum]. Return the number of ways a + b[ j] == sum where 0<=i < len(a) and 0<= j < len(b)
e.g a = [1,2,3] , b = [4,5]
queries = [[1,6], [0, 1, 2], [1,8]]
result = [2, 2]
for query 1, 6‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌ can come in 2 ways, 1 + 5 and 2 + 4
for query 2 -> update a[1] += 2 , so a becomes [1,4,3]
for query 3, 8 can come in 2 ways now as well. 4 + 4 and 5 + 3  
```

```java
```
