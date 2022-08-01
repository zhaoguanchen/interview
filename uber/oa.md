some experience 
1point3acres.com/bbs/thread-801493-1-1.html
<!--给定正整数n求0到n所有数字中024出现的次数之和10 0出现2次2和4分别出现1次返回422- 0出现32出现64出现2返回11-->

2brokenkeyboard



3messagesplit



https://www.1point3acres.com/bbs/thread-902780-1-1.html

新的

https://www.1point3acres.com/bbs/thread-915542-1-1.html



https://www.1point3acres.com/bbs/thread-907803-1-1.html

第1题，≈
<!-- 第2题， 给你y一个数组 nums, 每次往右边shift一个position看不能在shift几次之后让他变成从低到高sorted。nums = [4, 1, 2, 3] -> [3, 4, 1, 2] -> [2, 3, 4, 1] -> [1, 2, 3, 4] -> return 3 -->

第3题，给了你一个grid要你把这些俄罗斯方块给画在上面。 给了5个不同俄罗斯方块的图像， 没有绿色那个，但是有个只有一个tile的 （1x1)。可以assume一定放得下，尽量放越上面的row还有最靠近左边的column。

第4题,
给了你一个message queue 还有两个数组 a 跟 b，queue 里面有两种类型的讯息。第一种是 ‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌[0, i, x]， 要做的处理是 b += x。 第二个是 [1, x] 这代表你要找出 a + b[j] = x 然后把count 加到你的solution list里。 这题很看重runtime，跑太慢会fail至少6个hidden test case。



https://www.1point3acres.com/bbs/thread-906784-1-1.html

3. 给一个schedules，是list of list of list，里面是每个employee的meeting schedules，还给了一个integer length，代表要schedule meeting的长度。目的是要schedule这个长度为length的meeting，如果可以schedule，返回这个新meeting的start time，如果不能schedule(每个employees都没有长度为length的空闲时间)，返回-1. 如果看不明白可以看看下面的例子。
    比如schedules=[[[0, 80], [240, 360]], [[0, 60], [480, 600]]], length=120. 这个例子中employee 0 在0-80和240-360的时间段有meeting，employee 1在0-60和480-600的时间段有meeting，所以长度为120的新meeting最早能schedule到80，最后return 80.
    这一题当时太紧张了没有读完题目，后来发现有个条件没注意看，时间段是从0-1440（可能是因为一天只有1440分钟吧），所以最后的return的start time不能超过1440 - length，我忘记check了，所以有edge cases一直过不了。。。
4. 给两个array of integers，一个代表coordinates，一个代表colors，两个array长度都是n，返回一个长度为n的array of integers，代表到coordinate i时一共有多少unique colors。
    coordinates=[1, 2, 3, 3, 3, 5], colors=[1, 2, 2, 5, 4, 5]，返回results=[1, 2, 2, 3, 4, 4]。
    index=0时，coordinate 1被paint成了color 1， 这时候num of unique colors是1，所以results[0]=1.
    index=1时，coordinate 2被paint成了color 2，这时候num of unique colors是1和2，所以results[1]=2.
    index=2时，coordinate 3被paint成了color 2，这时候num of unique colors是1和2，所以results[2]=2.
    index=3时，coordinate 3被paint成了color 5，这时候num of unique colors是1，2和5，所以results[3]=3.
    index=4时，coordinate 3被paint成了color 4，这时候num of unique colors是1，2，5和4，所以results[4]=4.
    index=5时，coordinate 5被paint成了color 5，这时候num of unique colors是1，2，5和4，所以results[5]=4.
    这一题需要o(n)才能test cases全部过，我最后tle了，后来想了一下两个map就能做到o(n)，肯定也有更好的办法，求大神指教。
    总结：题很简单，但是题目是真的长，时间也比较紧张，所以我感觉更多的是考验心态。感觉越快做完分越高，还会penalize debug的时长，我试了一下practice exam，三分钟内做完第一道题，一次过，后面的题完全没看就submit都有667/850分。。。
    分数：每道题400分，前面两题满分，第三题280，第四题tle，过了10/20个test cases只有100分，这样算是980/1200，最后是727/850，怪自己时间一紧张，没有认真读题，所以第三题edge cases，debug一直弄不出来就心态崩了，一直死磕，最后没时间去优化第四题了。
    码字辛苦，也没加限制，求加米看面经，谢谢！！！
    补充内容 (2022-06-26 05:26 +8:00):[‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌/b]
    第四题有个小错误，修改一下：
5. 给两个array of integers，一个代表coordinates，一个代表colors，两个array长度都是n，返回一个长度为n的array of integers，代表到coordinate i时一共有多少unique colors。
    coordinates=[1, 2, 3, 3, 3, 5], colors=[1, 2, 2, 5, 4, 5]，返回results=[1, 2, 2, 3, 3, 4]。
    index=0时，coordinate 1被paint成了color 1， 这时候unique colors是1，所以results[0]=1.
    index=1时，coordinate 2被paint成了color 2，这时候unique colors是1和2，所以results[1]=2.
    index=2时，coordinate 3被paint成了color 2，这时候unique colors是1和2，所以results[2]=2.
    index=3时，coordinate 3被paint成了color 5，这时候unique colors是1，2和5，所以results[3]=3.
    index=4时，coordinate 3被paint成了color 4，这时候unique colors是1，2和4，所以results[4]=3.
    index=5时，coordinate 5被paint成了color 5，这时候unique colors是1，2，4和5，所以results[5]=4.

https://leetcode.com/problems/number-of-pairs-of-strings-with-concatenation-equal-to-target/



【第一题】
输入正整数数组A，返回01数组B，B[i]表示A[i] A[i+1] A[i+2]能否组成三角形。
【第二题】
<!--给一个长度为n的数组A，判断是不是由[1,2,...,n]或者[n,n-1,...,1]右移得来。比如[4,2,3,1]不是，[4,1,2,3]是。-->
【第三题】
给你二维数组长和宽，起点坐标，终点坐标。一开始从起点按照(+1, +1)的方式走，x坐标出界就取相反数，y出界同理，走到角落就同时取反。问走到终点的步数，如果走不到返回-1.
【第四题】
给一个数组，返回子数组个数，子数组满足‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌：所有元素都出现至少2次。
比如[1,2,1,2,4]返回1（[1,2,1,2]），[1,2,3,3,3,2,4]返回4（[3,3], [3,3], [3,3,3], [2,3,3,3,2]）





刚做了CodeSignal上的Uber OA，需要全程share full screen和开摄像头，还要受持证件照拍照。。一共四道题，每题300分。
1. <!--input一个String只包含“U”或“D”，代表向上或向下走一步，return最后的位移。-->
2. input一段文字，把里面的元音字母(a e i o u)每个都向后shift，最后一个元音字母放到第一个元音字母的位置，其他char都不变。
3. input两个array分别代表一些电池的使用时间和充电时间，给定一个目标时间t，先按照编号顺序使用电池，用完的立即开始充电，换下一个充满的电池（必须充满才能使用），没充好的就再换下一个，如果没有可用的return -1。如果能坚持到t，return num of fully used batteries.
4. 给a b两个array，给一个int[][] queries 代表指令，有一个指令只是改变b的某个值，另一个指令是找num of [i,j] pair in a and b such that a[i]+b[j]=target，return 指令产生的结果。
    总体不难，但是对复杂度有点‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌要求，有些hidden test case过不了。







https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=696384&ctid=230%26%238205%3B%26%238205%3B%26%238205%3B%26%238204%3B%26%238204%3B%26%238205%3B%26%238204%3B%26%238205%3B%26%238204%3B%26%238205%3B%26%238204%3B%26%238205%3B%26%238204%3B%26%238205%3B%26%238204%3B%26%238204%3B%26%238204%3B%26%238204%3B%26%238205%3B%26%238204%3B584



```
Quesiton 1
You are given an integer n. Your task is to calculate how many times the digits 0, 2 and 4 appear in all the non-negative integers up to n (0, 1, ...., n).
Example
• For n = 10, the output should be countOccurrences(n) = 4.
  ○ The digit 0 appears in numbers 0 and 10 once, for a total of 2 occurrences,
  ○ The digit 2 appears in the number 2 once, for a total of 1 occurrence,
  ○ The digit 4 appears in the number 4 once, for a total of 1 occurrence.So the answer is 2 + 1 + 1 = 4.
• For n = 22, the output should be countOccurrences(n) = 11.
  ○ The digit 0 appears in numbers 0, 10, and 20 once, for a total of 3 occurrences,
  ○ The digit 2 appears in numbers 2, 12, 20, and 21 once, and in the number 22 twice, for a total of 6 occurrences,
  ○ The digit 4 appears in numbers 4 and 14 once, for a total of 2 occurrences.So the answer is 3 + 6 + 2 = 11.
Input/Output
• [execution time limit] 4 seconds (py3)
• [input] integer nAn integer.Guaranteed constraints:0 ≤ n ≤ 1000.
• [output] integerThe overall count of occurrences of digits 0, 2 and 4 in the integers from 0 to n inclusive.
[Python 3] Syntax Tips
# Prints help message to the console# Returns a stringdef helloWorld(name):    print("This prints to the console when you Run Tests")    return "Hello, " + name
Quesiton 2
You are given a string str containing only the letters W, D, and L. Your task is to construct a new string from the characters of str, according to the following algorithm:
1. Begin with an empty string output = "".
2. If str contains a W, then remove it and concatenate a W to the end of output.
3. If str contains a D, then remove it and concatenate a D to the end of output.
4. If str contains an L, then remove it and concatenate an L to the end of output.
5. If str is empty, end the algorithm; otherwise go back to step 2.
Return the value of output after the algorithm is complete.
Note that it doesn't matter from where you remove the letter from the string, only the count of the letters left in the string matters.
Example
• For str = "LDWDL", the output should be equallyRearranging(str) = "WDLDL".
  ○ str contains all W, D, and L, so we add them to the output and remove from the initial string one by one and get "WDL"
  ○ The remaining string contains only letters D and L, so we add them to the output and get "WDLDL" as the answer
• For str = "DLDD", the output should be equallyRearranging(str) = "DLDD".
  ○ The string doesn't contain W letters, and do contain both D and L, so we add them to the output and remove from the initial string. The output is "DL" after that
  ○ The remaining string contains only two letters D and nothing else, so in two more iterations we get the output equal "DLDD"
Input/Output
• [execution time limit] 4 seconds (py3)
• [input] string strA string containing only the letters 'W', 'D' and 'L'.Guaranteed constraints:1 ≤ str.length ≤ 1000.
• [output] stringReturn the string constructed from the characters of str.
[Python 3] Syntax Tips
# Prints help message to the console# Returns a stringdef helloWorld(name):    print("This prints to the console when you Run Tests")    return "Hello, " + name
Question 3
You've decided to create a bot for handling stock trades. For now, you have a simple prototype which handles trades for just one stock. Each day, it's programmed to either buy or sell one share of the stock.
You are given prices, an array of positive integers where prices[i] represents the stock price on the ith day. You're also given algo, an array of 0s and 1s representing the bot's schedule, where 0 means buy and 1 means sell.
In order to improve the bot's performance, you'd like to choose a range of k consecutive days where the bot will be programmed to sell; in other words, set a range of k consecutive elements from algo to 1. Your task is to choose the interval such that it maximizes the bot's total revenue. The revenue is defined as the sum of all selling prices minus the sum of all buying prices (in other words, the difference between the end and start amount).
NOTE: Assume you begin with enough shares of the stock that it's always possible to sell.
Example
For prices = [2, 4, 1, 5, 2, 6, 7], algo = [0, 1, 0, 0, 1, 0, 0], and k = 4, the output should be maxRevenueFromStocks(prices, algo, k) = 21.
First, let's calculate the revenue if the algorithm is left as it is without any change.
• Before the trades start, the revenue is 0;
• Day 0: algo[0] = 0, so we buy stocks at price prices[0] = 2, and the revenue becomes 0 - 2 = -2;
• Day 1: algo[1] = 1, so we sell stocks at price prices[1] = 4, and the revenue becomes -2 + 4 = 2;
• Day 2: algo[2] = 0, so we buy stocks at price prices[2] = 1, and the revenue becomes 2 - 1 = 1;
• Day 3: algo[3] = 0, so we buy stocks at price prices[3] = 5, and the revenue becomes 1 - 5 = -4;
• Day 4: algo[4] = 1, so we sell stocks at price prices[4] = 2, and the revenue becomes -4 + 2 = -2;
• Day 5: algo[5] = 0, so we buy stocks at price prices[5] = 6, and the revenue becomes -2 - 6 = -8;
• Day 6: algo[6] = 0, so we buy stocks at price prices[6] = 7, and the revenue becomes -8 - 7 = -15.
Thus, the total revenue is -15.
We can maximize the total revenue by making the last k = 4 orders 1 (sell), thus making algo = [0, 1, 0, 1, 1, 1, 1]. The total revenue will become -2 + 4 - 1 + 5 + 2 + 6 + 7 = 21.
Input/Output
• [execution time limit] 4 seconds (py3)
• [input] array.integer pricesAn array of integers representing the stock price for each day.Guaranteed constraints:1 ≤ prices.length ≤ 105,1 ≤ prices[i] ≤ 1000.
• [input] array.integer algoAn array of 0s and 1s, representing the bot's buy / sell schedule for each day.Guaranteed constraints:algo.length = prices.length,0 ≤ algo[i] ≤ 1.
• [input] integer kAn integer representing the number of consecutive days that can be made all equal to 1, i.e. marked as sell.Guaranteed constraints:0 ≤ k ≤ prices.length.
• [output] integerThe value of the maximum revenue that can be obtained.
[Python 3] Syntax Tips
# Prints help message to the console# Returns a stringdef helloWorld(name):    print("This prints to the console when you Run Tests")    return "Hello, " + name
Question 4
You are given a square matrix of characters a which size is n x n. Your task is to create a list of strings from the diagonals of a, where each string has a length of n, and then sort this created list.
We'll consider all diagonals that are parallel to the main diagonal, where each diagonal is considered to start at its upper point and end at its lower point. Since these diagonals will have different lengths, we'll traverse each one cyclically (ie: go back to the start of the diagonal after reaching the end) until we reach n characters.
Sort the resulting strings in lexicographical order, and return an array of 2n - 1 integers, representing the diagonals' 1-based indices in their sorted order. In the case of lexicographically equal strings, their indices should be kept in the original order.
Here's an example of how to count the diagonals for a 5 x 5 matrix (the number on the diagram corresponds to the diagonal index):
5 6 7 8 94 5 6 7 83 4 5 6 72 3 4 5 61 2 3 4 5
Example
• Fora = [["b", "b"],     ["c", "a"]]the output should be diagonalsArranging(a) = [2, 3, 1].
       
This matrix has n = 2 and contains 3 diagonals:
  ○ The diagonal with index 1 is ["c"] and its corresponding cyclic string is "cc";
  ○ The diagonal with index 2 is ["b", "a"] and its corresponding cyclic string is "ba";
  ○ The diagonal with index 3 is ["b"] and its corresponding cyclic string is "bb".The lexicographical ordering of the matrix diagonals looks like ["ba", "bb", "cc"], so the answer is [2, 3, 1].
• Fora = [["a", "c", "a", "b", "b"],      ["c", "b", "a", "c", "b"],      ["a", "a", "e", "c", "b"],      ["b", "b", "d", "a", "g"],      ["a", "b", "e", "b", "a"]]the output should be diagonalsArranging(a) = [1, 5, 3, 7, 2, 8, 9, 6, 4].
       
This matrix has n = 5 and contains 9 diagonals:
  ○ The diagonal with index 1 is ["a"] and its corresponding cyclic string is "aaaaa",
  ○ The diagonal with index 2 is ["b", "b"] and its corresponding cyclic string is "bbbbbb",
  ○ The diagonal with index 3 is ["a", "b", "e"] and its corresponding cyclic string is "abeab",
  ○ The diagonal with index 4 is ["c", "a", "d", "b"] and its corresponding cyclic string is "cadb‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌c",
  ○ The diagonal with index 5 is ["a", "b", "e", "a", "a"] and its corresponding cyclic string is "abeaa",
  ○ The diagonal with index 6 is ["c", "a", "c", "g"] and its corresponding cyclic string is "cacgc",
  ○ The diagonal with index 7 is ["a", "c", "b"] and its corresponding cyclic string is "acbac",
  ○ The diagonal with index 8 is ["b", "b"] and its corresponding cyclic string is "bbbbb",
  ○ The diagonal with index 9 is ["b"] and its corresponding cyclic string is "bbbbb".The lexicographical ordering of the matrix diagonals looks like ["aaaaa", "abeaa", "abeab", "acbac", "bbbbb", "bbbbb", "bbbbb", "cacgc", "cadbc"], so the answer is [1, 5, 3, 7, 2, 8, 9, 6, 4].Note that the cyclic string "bbbbb" occurs 3 times, and the indices corresponding to this cyclic string appear in ascending order in the output: [2, 8, 9].
Input/Output
• [execution time limit] 4 seconds (py3)
• [input] array.array.char aA square matrix of characters. It is guaranteed that the characters in the matrix are all lowercase English letters.Guaranteed constraints:2 ≤ a.length ≤ 100,a[i].length = a.length.
• [output] array.integerAn array of size 2n - 1, containing the indices of the diagonals after sorting.
[Python 3] Syntax Tips
# Prints help message to the console# Returns a stringdef helloWorld(name):    print("This prints to the console when you Run Tests")    return "Hello, " + name
```



```
第一题:
给一个数组，检查连续两个数字是否同为奇数或者偶数。如果是，则返回第一个数的位置。
例子：
给定[1,4,7,5,2], 返回3.
1 是奇数， 4是偶数，7是奇数，5是奇数。第一个符合要求的数字是7，位置是3.
第二题：
给两个机场A和B，以及飞机起飞的时间a list 和 b list, 以及往返的次数 (A->B->A) 算一次。飞行时间固定为100分钟。返回完成往返次数之后的时间 (到达A的时间).
例子：
A机场起飞时间 [0, 99, 201, 500]
B机场起飞时间 [101, 150, 600]
往返次数 - 2 次。
第一个往返 - A 0 时起飞，100分钟时到达B。 然后B 101分钟时起飞，201分钟时到达A。
第二个往返 - A 201 分钟时起飞， 301分钟时到达B。 然后B 600 分钟时起飞，700 分钟时到达A。
返回700.
第三题:
太长，略过。
第四题:
给一个数组[1,2,1,1], 一个 k 值 = 2, 返回满足条件的subarray的数量 - 条件时 - subarray当中必须含有至少k个只出现过1次的数字。
例子:
数组[1,2,1,1], k = 2, 返回2.
满足条件的subarray 包括 - [1,2], [2,1]
[1,2,1] 不满足，因为只有2出现了1次。
数组[1,2,3,4,1], k =3, 返回6‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌.
满足条件的subarray 包括 - [1,2,3], [1,2,3,4],[1,2,3,4,1],[2,3,4],[2,3,4,1],[3,4,1]
其中[1,2,3,4,1] 满足，因为出现过1次的数字有[2,3,4], length >= k.
```



```
Given an array of strings, your task is to find the number of pairs in which one string is a suffix
of the other string. Specifically, given 0 <= i < j < strings.length,
strings can be a suffix of strings[j], or strings[j] can be a suffix of strings
参考思路：
1. Reverse all strings in the array
2. Sort
3. For each string, binary search

def func():
    strings = ['cba',"a","a","b","ba","ca"]
    strings = list(map(lambda x:x[::-1], strings))
    sorted_strings = sorted(strings)
    length = len(sorted_strings)
    ans = 0
    for i in range(len(sorted_strings) - 1):
        current = sorted_strings[ i ]
        first_not_ok = bi_search(sorted_strings, current, i+1, length)
        ans += first_not_ok - i - 1
    return ans
def bi_search(strings, prefix, lo, hi):
    while lo < hi:
        mid = (lo + hi) // 2
        string = strings[mid]
        if prefix != string[:len(prefix)]:
            hi = mid
        else:
            lo = mid + 1
[in‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌dent]    return lo
print(func() == 8)
```





```
Codesignal 给4道题目

3. 2d matrix 三种操作。rotate 90， left对角线flip，right对角线flip。最后得到什么-baidu 1point3acres
4. 给一个array 可以 +N 或者 -N。 -N 是移除里面的element。给一个difference=k，问每次加一个value，那个list里面可有对少对pair满足difference=k。
```



```
https://www.1point3acres.com/bbs/thread-876371-1-1.html
推箱子

```



# 高频

## 024

```
给定正整数n，求0到n所有数字中0， 2， 4出现的次数之和
10 --> 0出现2次，2和4分别出现1次，返回4
22 --> 0出现3， 2出现6，4出现2，返回11
```

```java
class CountOccurrences {

    public int helper(int n) {
        int result = 0;

        while (n > 0) {
            int reminder = n % 10;
            if (reminder == 0 || reminder == 2 || reminder == 4) {
                result++;
            }
            n = n / 10;
        }
      
        return result;
    }

    public int number(int n) {
        int count = 1;
        for (int i = 1; i <= n; i++) {
            count += helper(i);
        }
        return count;
    }

    public static void main(String[] args) {
        CountOccurrences oc = new CountOccurrences();
        int total = oc.number(22);
        System.out.println(total);

    }

}

```



## shift array

```
一个array 可以往左shift K 次。问是否能得倒一个sorted 从小到大 array

给一个array of integers，里面的数是1到n（没有重复的数），n是array的长度，return需要把array右移多少步能够把这个array变成[n, n-1, n-2, ..., 1]，如果不可能就return -1. 比如input=[2, 1, 4, 3], return=2,因为向右移两步之后array能变成[4, 3, 2, 1]; input=[1, 2, 3, 4], return=-1,因为向右移多少步，都不可能把array变成[4, 3, 2, 1]。
```

```java
     public int shift(int[] nums) {
        int n  = nums.length;
        int count = 0;
        int index = 0;
        for (int i = 0; i < n; i++) {
          if (nums[i] < nums[(i + 1) % n]) {
            count++;
            index = i;
          }

          if (count > 1) {
            return -1;
          }
				 return  n - 1 - index;
 
}
```

## U and D

```
机器人只能U和D，给一个array包含UD，问最后结果
```

```
给一个string of operations，里面只有u或者d，u等于往上位移，d等于往下位移，return在operations之后的位置是u还是d，如果回到原点，return一个whitespace。
比如input=‘ududdd’，return=‘d'；input=‘ududud’，return=‘ ’。这一题我就数了一下string里面u和d的数量，然后对比一下就行了。
```
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
given two arrays a and b and list of queries. Return the values of all (1) query in an array.
Queries are of two types:
(0) update [type, index of element in a, value]. Update the element in a by given value
(1) get [type, sum]. Return the number of ways a + b[ j] == sum where 0<=i < len(a) and 0<= j < len(b)
e.g a = [1,2,3] , b = [4,5]
queries = [[1,6], [0, 1, 2], [1,8]]
result = [2, 2]
for query‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌ 1, 6 can come in 2 ways, 1 + 5 and 2 + 4
for query 2 -> update a[1] += 2 , so a becomes [1,4,3]
for query 3, 8 can come in 2 ways now as well. 4 + 4 and 5 + 3  


```


```java
```







## same letter

```
给一个String Array strs[ ], return含3个及以上相同字母的string的个数
```

```
在一个类似于str="aaa bbb ccd"中数出重复字母超过三个的个数，比如现在就是aaa,bbb符合条件，所以return 2
```

```java
class Solution {
  public int count(String[] strs) {
    int ans = 0;
    
    for (String s : strs) {
      int[] count = new int[26];
      for (int i = 0; i < s.length(); i++) {
        count[s.charAt(i) - 'a']++;
        if (count[s.charAt(i) - 'a'] == 3) {
          ans++;
          break;
        }
      }
    }

    return ans;
  }
}
```



## sub array

```
给一个数组[1,2,1,1], 一个 k 值 = 2, 返回满足条件的subarray的数量 - 条件时 - subarray当中必须含有至少k个只出现过1次的数字。
例子:
数组[1,2,1,1], k = 2, 返回2.
满足条件的subarray 包括 - [1,2], [2,1]
[1,2,1] 不满足，因为只有2出现了1次。
数组[1,2,3,4,1], k =3, 返回6‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌.
满足条件的subarray 包括 - [1,2,3], [1,2,3,4],[1,2,3,4,1],[2,3,4],[2,3,4,1],[3,4,1]
其中[1,2,3,4,1] 满足，因为出现过1次的数字有[2,3,4], length >= k.
```

```java
```



##  WDL

```
You are given a string str containing only the letters W, D, and L. Your task is to construct a new string from the characters of str, according to the following algorithm:
1. Begin with an empty string output = "".
2. If str contains a W, then remove it and concatenate a W to the end of output.
3. If str contains a D, then remove it and concatenate a D to the end of output.
4. If str contains an L, then remove it and concatenate an L to the end of output.
5. If str is empty, end the algorithm; otherwise go back to step 2.
Return the value of output after the algorithm is complete.
Note that it doesn't matter from where you remove the letter from the string, only the count of the letters left in the string matters.
Example
• For str = "LDWDL", the output should be equallyRearranging(str) = "WDLDL".
  ○ str contains all W, D, and L, so we add them to the output and remove from the initial string one by one and get "WDL"
  ○ The remaining string contains only letters D and L, so we add them to the output and get "WDLDL" as the answer
• For str = "DLDD", the output should be equallyRearranging(str) = "DLDD".
  ○ The string doesn't contain W letters, and do contain both D and L, so we add them to the output and remove from the initial string. The output is "DL" after that
  ○ The remaining string contains only two letters D and nothing else, so in two more iterations we get the output equal "DLDD"
Input/Output
• [execution time limit] 4 seconds (py3)
• [input] string strA string containing only the letters 'W', 'D' and 'L'.Guaranteed constraints:1 ≤ str.length ≤ 1000.
• [output] stringReturn the string constructed from the characters of str.
```

```java
class SolutionHelper {
  
  
    public String helper(String s) {
        Map<Character, Integer> map = new HashMap<>();
        map.put('W', 0);
        map.put('D', 0);
        map.put('L', 0);
        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            map.put(c, map.get(c) + 1);
        }

        StringBuilder sb = new StringBuilder();
        int total = s.length();
        while (total > 0) {
            if (map.get('W') > 0) {
                sb.append("W");
                total--;
                map.put('W', map.get('W') - 1);
            }

            if (map.get('D') > 0) {
                sb.append("D");
                total--;
                map.put('D', map.get('D') - 1);
            }

            if (map.get('L') > 0) {
                sb.append("L");
                total--;
                map.put('L', map.get('L') - 1);
            }

        }

        return sb.toString();

    }


}
```





## 二进制数加一

```
给一个字符串形式的二进制数，给一个query list，query有两种，'+'是把那个二进制数加一，'?'

\1. 2.

是在返回list中加入二进制字符串中'1'的个数 比如说，input='1110'， query=[?,+,?,+,+,?]

return [3， 4， 2]
```

```java

    public List<Integer> countSubStr(String str, List<String> ops) {
        int num = 0;

        for (int i = str.length() - 1; i >= 0; i--) {
            if (str.charAt(i) == '1') {
                num += Math.pow(2, str.length() - 1 - i);
            }
        }

        List<Integer> ans = new ArrayList<>();
        for (String o : ops) {
            if ("?".equals(o)) {
                ans.add(countOne(num));
            } else {
                num++;
            }
        }

        return ans;
    }

    private int countOne(int n) {
        int ans = 0;
        while (n > 0) {
            ans++;
            n = n & (n - 1);
        }

        return ans;
    }
```



## radius

```
大意是 input是一个matrix和一个radius，这个radius表示一个element到中心 element的euclidean distance。一个元素和自己的距离是1.然后对matrix里每一个可能的 center，求关于这个center距离为radius的元素的和。大概是这样:

1,2,3,4,5 radius = 3， 那么唯一一个valid的center是正中间的那个3，因为其他的元素 作为 center的话，距离为3会超出边界。结果就是3+4+5+4+3+2+1+2=24

1,2,3,4,5
 1,2,3,4,5
 1,2,3,4,5
 1,2,3,4,5
 这个题弯弯绕挺多的，我用print debug法debug了很久才过了所有test

```



2.  



## word

```
eg. str = [
["1", "Hello how r u"]
["2", "Good u"]
["1", "Good"]
],
width = 15, userwidth = 5
output = [
"+***********+"
"|Hello         |"
"|how r        |"
"|u               |"
‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌
"|        Good|"
"|               u|"
"|Good        |"
"+***********+"
]
```

```java
```



 

# 一亩三分地



第一题：很简单所以忘了。。
第二题：在一个类似于str="aaa bbb ccd"中数出重复字母超过三个的个数，比如现在就是aaa,bbb符合条件，所以return 2
第三题：在几个4*4 matrix中各找一个missing element，marked by '?’，然后找到的element的大小给这些matrices排序，如果都一样则保持原顺序
第四题：给定a，b，比如a=[1,2,3], b=[4,5]；同时给定一个list of queries，query有两种情况：（1）比如[0,1,x]，0就是a，1就是指a中的index为1，x指的是a[index] = x，这个操作不需要对res进行更新； (2）比如[1,m]，即输出a，b中相加等于m的所有情况的数量，比如m=5, 那么只有1+4符合情况，则‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌res.append(1)。 值得一提的是这题对时间复杂度要求比较高
目前uber的oa应该很多在codesignal上面进行，推荐大家先做practise熟悉一下平台。

 一个城市有三个区域 A， B， C。 是从A到C的包含关系。（A是B的子区域，B是C的子区域）
给input三个list，是list of strings for 地铁站名。 另有input 两个string，是origin 和destination站名。
地铁票有三种，AB，  BC， ABC。价格按照这个顺序便宜到贵。
问给定的两站之间最便宜的地铁票是这三种的哪一种。如果站名不存在return “”。



## sum

```
給定一個array，回傳符合條件(arr + arr[i+1] + arr[i+1]) > (arr[i-1] + arr + arr[i+1])的數量
範例:
arr = [1, 3, 4, 2, 3, 4, 1]
i = 1: (arr + arr[i+1] + arr[i+1]) = 9 / (arr[i-1] + arr + arr[i+1]) = 8 => 符合條件 cnt++
i = 2: (arr + arr[i+1] + arr[i+1]) = 9 / (arr[i-1] + arr + arr[i+1]) = 9 => 不符合條件
i = 3: (arr + arr[i+1] + arr[i+1]) = 9 / (arr[i-1] + arr + arr[i+1]) = 9 => 不符合條件
i = 4: (arr + arr[i+1] + arr[i+1]) = 8 / (arr[i-1] + arr + arr[i+1]) = 9 => 不符合條件
回傳return = 1
解法: O(n)
遍尋一次input array做accumulate sum array，然後再遍尋一次input array求解
```

```java
    // 1, 3, 4, 2, 3, 4, 1
    // 0, 1, 4, 8, 10, 13, 17, 18
    public int sum(int[] nums) {
        int[] sum = new int[nums.length + 1];
        sum[0] = nums[0];
        for (int i = 1; i < nums.length; i++) {
            sum[i + 1] = nums[i] + sum[i];
        }
        int count = 0;
        for (int i = 4; i < sum.length; i++) {
            if (sum[i] - sum[i - 3] > sum[i - 1] - sum[i - 4]) {
                count++;
            }
        }

        return count;
    }
```



## appearence

```
給另一個String arr還有一個string s，要回傳arrayList中的string有多少種在s中出現的字元。
0<= s.length <= 26, s中沒有重複。
arr中的string和s均為lowercase。
範例:
arr = ["banana", "apple", "orange"], string s = "abe"
"banana" => 有a有b => 2 (注意是有兩個，不是累積baaa有四個)
"apple" => 有a有e => 2
"orange" => 有e => 1
回傳return = [2, 2, 1]
解法: 26*O(m*n) // arr長度為m，裡頭的string長度為n
把string s轉成dictionary set (我用int[26]來做)。
array中個每一個string在轉成set去查找。
```





## move robot

```
給定n*m的map，map上面的robot起始位置(x1, y1)，還有一個目標位置(x2, y2)。問你這個robot要移動多少步才能從起始位置抵達目標位置。如果無法抵達回傳-1。
Robot的前進規則如下:
1. 一開始往 (右, 下) 移動
2. 如果下一步的移動會超出map boundry，則根據超出的位置轉換方向 (所以不會超出boundry，但是這裡還是要算移動一步)。
如果往 (右, 下) 的下一步會超過 x-boundry，則不移動，轉換方向到 (左, 下)。
如果往 (右, 下) 的下一步會同時超過 x-boundry以及y-boundry (也就是從右下角出界)，則不移動，轉換方向到 (左, 上)。
範例:
map: 4*5, (x1, y1)‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌ = (1, 0), (x3, y2) = (0,3)

回傳return = 7
解法: O(m*n)
其實只是題目敘述比較複雜，理解之後就照著他的移動邏輯去移動robot就好
用一個set去存走過的地方和方向 (要存方向，有可能你會走到之前走到的地方，但是繞回去還是可以抵達終點的)。
```



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

## pair of prefix

```
nput是 a list of strings。问有多少个 i， j 的 index pair，such that strings 是 strings[j] 的prefix。
return pair 个数

排序 + 二分
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







