# 整理后的oa

## 1. minimum days to deliver all the parcels
Keyword:parcels,deliver

Find minimum nunmber of days needed to deliver all the parcels.

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


## 2. Password strength == [leetcode 2262] Total Appeal of A String

assume we have string xxxaxxxxb..., with s[i] = a and s[j] = b.
s[i] is th last character a before that b.

We want to count, how many substring ending at s[j] contains character a.
They are xxxaxxxxb, xxaxxxxb, xaxxxxb, axxxxb ....,
i + 1 substring ending with character a at s[i],
so we do res += i + 1.

We repeatly do this for every s[i] and every one of 26 characters.

```java
    public long appealSum(String s) {
        
        int[] memo = new int[26];
        
        char[] chars = s.toCharArray();
        long count = 0;
        
        for (int i = 0; i < chars.length; i++) {
            memo[chars[i] - 'a'] = i + 1;
            
            for (int position : memo) {
                count += position;
            }
            
        }
        
        return count;
        
    }
```



## 3. Economy Mart

Use both min heap and max heap
The size of max heap will be equal to the kth query as top of max heap will contain the kth cheapest element.
If the size of max heap is less than kth query add item to max heap directly.
Else If the price of new item to be inserted is less than the price of item at the top, remove the top item of max heap and insert into min heap and add new item into max heap.

```java
class EconomyMartSolution {

    public String[] tracker(String[][] operations) {
        EconomyMartTracker tracker = new EconomyMartTracker();
        List<String> ans = new ArrayList<>();
        for (String[] operation : operations) {
            if ("VIEW".equals(operation[0])) {
                ans.add(tracker.get());
            } else {
                tracker.add(operation[1], operation[2]);
            }
        }

        String[] res = new String[ans.size()];

        for (int i = 0; i < res.length; i++) {
            res[i] = ans.get(i);
        }

        return res;


    }

}

class EconomyMartTracker {

    private PriorityQueue<EconomyMartTrackerEntity> minHeap;

    private PriorityQueue<EconomyMartTrackerEntity> maxHeap;


    public EconomyMartTracker() {
        // candidate element
        this.maxHeap = new PriorityQueue<>((a, b) -> {
            if (a.score == b.score) {
                return a.name.compareTo(b.name);
            }
            return a.score - b.score;
        });

        // processed element
        this.minHeap = new PriorityQueue<>((a, b) -> {
            if (a.score == b.score) {
                return b.name.compareTo(a.name);
            }
            return b.score - a.score;
        });

    }

    public void add(String name, String score) {
        EconomyMartTrackerEntity entity = new EconomyMartTrackerEntity(name, Integer.parseInt(score));
        minHeap.add(entity);
        maxHeap.add(minHeap.poll());
    }

    public String get() {
        EconomyMartTrackerEntity candidate = maxHeap.poll();
        minHeap.add(candidate);
        return candidate.name;
    }
}


class EconomyMartTrackerEntity {

    int score;
    String name;

    public EconomyMartTrackerEntity(String name, int score) {
        this.name = name;
        this.score = score;
    }
}
```





## 4. find plan for the closest X destinations


 **PriorityQueue**
```java
// "static void main" must be defined in a public class.
//Input
// allLocations = [ [1,2], [3,4], [1,-1]]
// numDeliveries = 2

// output
// [ [1,-1], [1,2]]
public class Main {
    public static void main(String[] args) {
        int[][] points = {{1,2}, {3,4}, {1, -1}};
        int k = 2;
        Solution solution = new Solution();
        int[][] ans = solution.kClosest(points, k);
        System.out.println(Arrays.deepToString(ans));
    }
}

class Solution {
    
    public int[][] kClosest(int[][] points, int k) {
        
        PriorityQueue<int []> pq = new PriorityQueue<>((a, b) -> {
            int distanceA = getDistance(a);
            int distanceB = getDistance(b);
            
            if (distanceA == distanceB) {
                return Math.abs(a[0]) - Math.abs(b[0]);
            } else {
                return distanceA - distanceB;
            }
        });
        
        for (int[] point : points) {
            pq.add(point);
        }
        
        int[][] ans = new int[k][2];
        
        for (int i = 0; i < k; i++) {
            ans[i] = pq.poll();
        }
        
        return ans;
        
    }
    
    private int getDistance(int [] point) {
        return point[0] * point[0] + point[1] * point[1];
    }
}
```


## 5. max de‍‌‌‍‌‍viation among all substrings



## 6. Count Decreasing Ratings

https://leetcode.com/playground/UEQFLjEn

```java
class Solution {
  
    public int countDecreasingRatings(int[] ratings) {
        if (ratings.length == 0) {
            return 0;
        }
        int left = 0;
        int ans = 0;

        for (int right = 0; right < ratings.length; right++) {
            if (right - 1 < 0) {
                ans++;
                continue;
            }
            if ((ratings[right - 1] - ratings[right]) == 1) {
                ans += (right - left + 1);
            } else {
                left = right;
                ans += 1;
            }

        }
        return ans;
    }
}
  
```


## 7. [Leetode 2272] Substring With Largest Variance
Time Complexity= O(26*26*n)

For every possible character pair a(min freq) & b(max freq),
find the substring with the max differenct between the freq of a & b which can be done using kadanes algorithm.

We can think about it as finding the maximum subarray with a = -1 and b = 1 and other characters = 0. But we should have at least one occurrence of a.

```java
class Solution {
    public int largestVariance(String s) {

        int[] count = new int[26];
        char[] chars = s.toCharArray();

        for (char c : chars) {
            count[c - 'a']++;
        }

        int maxVariance = 0;

        for (int i = 0; i < 26; i++) {
            for (int j = 0; j < 26; j++) {
                int totalI = count[i];
                int totalJ = count[j];

                if (i == j) {
                    continue;
                }

                if (totalI == 0 || totalJ == 0) {
                    continue;
                }

                int currentI = 0;
                int currentJ = 0;
                for (int k = 0; k < chars.length; k++) {

                    int c = chars[k] - 'a';
                    if (c == i) {
                        currentI++;
                    } else if (c == j) {
                        currentJ++;
                        totalJ--;
                    }

                    if (currentJ > 0) {
                        maxVariance = Math.max(maxVariance, currentI - currentJ);
                    }

                    if (currentI < currentJ && totalJ > 0) {
                        currentI = 0;
                        currentJ = 0;
                    }

                }
            }
        }

        return maxVariance;
    }
}
```

## 8. Server Power [Find Maximum Sustainable Cluster Size]

https://leetcode.com/playground/XHaDvGTH

```java
class Solution {


    public int maxLengthValidSubArray(int[] processingPower, int[] bootingPower, int maxPower) {
        if (processingPower == null || bootingPower == null || processingPower.length != bootingPower.length) {
            return 0;
        }
        if (processingPower.length == 0 || maxPower == 0) {
            return 0;
        }
        PriorityQueue<Integer> pq = new PriorityQueue<>((a, b) -> {
            return b - a;
        });


        int maxLength = 0;
        int currentLength = 0;

        int left = 0;
        int right = 0;

        int processingPowerSum = 0;
        while (right < processingPower.length) {

            pq.add(bootingPower[right]);
            processingPowerSum += processingPower[right];
            currentLength++;

            int maxBootingPower = pq.peek();
            int sum = maxBootingPower + processingPowerSum * currentLength;

            if (sum <= maxPower) {
                maxLength = currentLength;
                right++;

            } else {
                processingPowerSum -= processingPower[left];
                pq.remove(bootingPower[left]);
                left++;
                right++;
                currentLength--;
            }


        }

        return maxLength;
    }
}


```


## 9. maximize the median sum

```java


```



## 10. Amazon Warehouse

Given the weights of the n items and an integer k, fine the number of segments of items that can be shipped together.

```java
public int shipment(int [] arr, int k){

int left = 0;
int count = 0;
Deque<Integer> incr = new LinkedList<Integer>(); //  to store the index of min values at each iteration 
Deque<Integer> decr = new LinkedList<Integer>(); // to store the index of max values at each iteration

for(int right = 0; right<arr.length;right++){
 
 while(!incr.isEmpty() && arr[right] <= arr[incr.peekLast]){ //remove value from the end until the current value is greater than the last value in the queue
           incr.pollLast();
 }
incr.offerLast(right);

while(!decr.isEmpty() && arr[right] >= arr[decr.peekLast]){ //remove value from the end until the current value is less than the last value in the queue
        decr.pollLast();
}


while(arr[decr.peekFirst()] - arr[incr.peekFirst()] > k){//slide the window if the diff between min and max is bigger than k
     if(decr.peekFirst() <= left)
          decr.pollFirst();
     if(incr.peekFirst() <= left)   
         incr.pollFirst();
    left++;
}

 count+= right-left+1;






}

return count;

}
```

