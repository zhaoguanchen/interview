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


## 2. [leetcode 2262] Total Appeal of A String





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
