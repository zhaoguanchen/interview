# Expedia

selling products和grouping options

https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=805661&highlight=Expedia%2Boa



1. Device Name System
2. Comparator 這邊只能用C++或JAVA寫
3. Prison Break

1. compress string：input "abcaabbc" -> output "abca2b2c"
2. 蠡口 药物令其 reformat date："3rd Jan 2012" -> "2012-01-03", 注意input是多个string，所以在里扣代码外再多加一层for.



```
1. 按照要求 改写comparator 实现三个compare {int a, int b , a==b}, {string a, string b, a == b} , {int[] a. int[] b, a[i] == b[i]}  
2. Math homework 给了一个排序好的数列，代表学生要解决的问题，它如果选了0号作业，如果不选1号作业，就得选2号。给了阈值，要求作业的最大值-最小值之差大于等于阈值，如果不行就得把所有作业都完成。问学生需要完成的最小数量的作业。固定第0号作业，二分搜索找到第一个数字大于等于阈值-0号作业的index，如果不存在返回整个数组值，存在，返回这段长度的/2。
3. given a sum of element‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌ n and number of elements k, find the number of distinct arrays under those conditions.


```



```
Create a Comparator class: Overload method compare(int a,int b),  compare(String a,String b), compare(int[] a,int[] b
lc 1492 The kth Factor of n: https://leetcode.com/problems/the-kth-factor-of-n/
lc 1197 Minimum Knight Moves: https://leetcode.com/problems/minimum-knight-moves/  Given the start and target, find the minimum steps after moves
```



 

```
90min 三道题 SDE II
1. Delivery Management System
2. lc!$(@ kth factor of n
3. Scat‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌ter Palindrome
```



```
地里内推，隔天收OA
90min 3题 都是地里出现过的
1. 打印用户名，第一次出现的直接打印，后面又重复的就在名字后面加数字，从1开始累加
2. Math Homework
3. Scatter Palindrome
地里常见题。
1.  按照要求 改写comparator 实现三个compare {int a, int b , a==b}, {string a, string b, a == b} , {int[] a. int[] b, a == b}  
2. Math homework.  input: 无序list (代表math homework point) 和 threshold。做题顺序是after solving ith problem, you can solve i + 1 or i + 2
问最少做几个homework，能使：你的得分中最高分减最低分>= threshold
3. given a sum of element n and number of elements k,‍‌‌‌‌‌‌‍‌‌‍‍‍‌‍‍‍ find the number of distinct arrays under those conditions.
4. 将x个人分到y个组里，要求是每个组的人数要大于等于其左边组的人数，比如8个人分4个组，分法有【1，1，1，5】，【1，2，2，3】等等等。要求算出所有可能的组合总数。
5. ‍‍‌‍‍‍ Scatter Palindrome：计算substring经过rearrange可‍‌‌‌‌‌‌‍‌‌‍‍‍‌‍‍‍以变成palindrome的substring个数 https://image.slidesharecdn.com/neerc2012problemreview-121202061050-phpapp01/95/acm-icpc-2012-neerc-northeastern-european-regional-contest-problems-review-9-638.jpg
6. 求[a,b]之间的以3，5为底的数字 比如3^2*5^3 这样的数字 这个题参考刷题网而留司 一个一个构造就行了
7. 股票题，刷题网伊尔①，返回的时候注意，如果返回0，改成-1。
8. Prison题，https://www.chegg.com/homework-h ... paced-one-q54963882， 答案在这里，‍‌‌‌‌https://github.com/kaushal02/int ... ter/prisonBreak.cpp
9. 给两个字符串，先判断第二个是否可以连续打印形成第一个。如果不可以返回-1，如果可以在第二个字符串中找到最短的字符串，可以通过连续打印最短字符串形成第一个和第二个字符串，返回最短字符串的长度。
10. 刷题网意思久而
11. 返回一个数的第四个比特位是1还是0
12. 一个数列里找最大的任意组合之和并且该组合的和要小于或等于阈值。
补充内容 (20‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌21-09-04 03:46 +8:00):

```

## Scatter Palindrome 

```
https://leetcode.com/discuss/interview-question/431933/rubrik-oa-2019-scatter-palindrome
```



```
device name  and metro land festival
https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=858437&highlight=Expedia%2Boa
```

```
121. Best Time to Buy and Sell Stock
以下内容需要积分高于 188 您已经可以浏览
1492. The kth Factor of n
1197.  Minimum Knight Moves
```

```
第一题：一丝霸气
第二题：一丝久儿
第三题：Scatter Palindrome
```



```
https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=864869&highlight=Expedia%2Boa
第一题 math homework https://leetcode.com/discuss/int ... es-of-math-problems
第二题 device name system，类似李叩一丝霸气，比这道还简单，限制了input string只有字母没有数字
第三题 scatter palindrome，https://leetcode.com/discuss/int ... lindrome-Discussion
```

```
https://leetcode.com/problems/minimum-knight-moves/solution/
```



## metro land festival

```java
int cost(x, y, a, b) {
   return (abs(x-a)+abs(y-b));
}
int greedy(vector<int> numpeople, vector<int> x, vector<int> y){
    vector<int> xx, yy;
    int ans = 0;
    for(int i = 0 ; i < numpeople.size();i++){
        int count = numpeople[i];
        while(count--){
            xx.push_back(x[i]);
            yy.push_back(y[i]);
        }
    }

    sort(xx.begin(), xx.end());
    sort(yy.begin(), yy.end());
    int mx, my;

    mx = xx[xx.size() / 2];
    my = yy[yy.size() / 2];

    for(int i = 0; i < numpeople.size();  i++){
        ans += numpeople[i] * cost(mx, my, x[i], y[i]);
    }
    return ans;
}
```



```java
class Solution {
    public int kthFactor(int n, int k) {
        List<Integer> divisors = new ArrayList();
        int sqrtN = (int) Math.sqrt(n);
        for (int x = 1; x < sqrtN + 1; ++x) {
            if (n % x == 0) {
                --k;
                divisors.add(x);
                if (k == 0) {
                    return x;    
                }    
            }    
        }
        
        // If n is a perfect square
        // we have to skip the duplicate 
        // in the divisor list
        if (sqrtN * sqrtN == n) {
            ++k;    
        }
                
        int nDiv = divisors.size();
        return (k <= nDiv) ? n / divisors.get(nDiv - k) : -1;
    }
}
```



## device name

```java
class Solution {
    public String[] getFolderNames(String[] names) {
        Map<String, Integer> nameMap = new HashMap<>();
        int n = names.length;
        String[] res = new String[n];
        for (int i = 0; i < n; i++) {
            if (!nameMap.containsKey(names[i])) {
                nameMap.put(names[i], 1);
                res[i] = names[i];
            }
            else {
                int val = nameMap.get(names[i]);
                String name = names[i] + "(" + val + ")";
                while (nameMap.containsKey(name)) {
                    name = names[i] + "(" + ++val + ")";
                }
                res[i] = name;
                nameMap.put(names[i], ++val);
                nameMap.put(name, 1);
            }
        }
        return res;
    }
}
```



选择题

https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=811490&highlight=Expedia%2Boa