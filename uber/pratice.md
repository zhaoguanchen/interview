# Uber VO




BQ 
https://www.1point3acres.com/bbs/thread-668855-1-1.html


System Design

## 推荐文章
https://mecha-mind.medium.com/system-design-nearby-places-recommender-system-7ac53e27c977


## heat map


https://www.1point3acres.com/bbs/thread-913657-1-1.html


## stock push

https://www.1point3acres.com/bbs/thread-907582-1-1.html

 SD，设计一个Uber eats的系统返回用户附近可选的餐馆‍‍‍‌‌‍‌‍‌‍‌‍‌‍‌‌‌‌‍‌





## pratice

### 

### breakingBad
```
You're given a set of symbols for the elements in the periodic table [.... Li, Be, B, C, N, F, Ne, Na, Co, Ni, Cu, Ga, Al, Si.....]

Write the function breakingBad(name, symbols) that given a name and a set of symbols returns the phrase with the following format [Symbol]rest of the word

Example:
symbols = [H, He, Li, Be, B, C, N, F, Ne, Na, Co, Ni, Cu, Ga, Al, Si, Fa]
breakingBad("henry alba", symbols) results in [He]nry [Al]ba

Follow up: we only care about the longest symbol within a word. Example in the word henry there are two elements that are present [H] & [He] and we want He in the output phrase and not H.

I am wondering how you would approach this problem?

My attempt to solving this during the interview was:

Put the symbols in a set for constant lookup time.
Find the maxLen of any symbol.
Break up the given string into multiple words (the only delimiter will be a blank space)
For each word look for the maxLen substring and then recurse on that substring with maxLen - 1 till maxLen == 0; and do that for each substring that can be formed.
This seems like a brute force approach to me, I am wondering how best to optimize it which is why I am writing this post.
```