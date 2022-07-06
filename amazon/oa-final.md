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


