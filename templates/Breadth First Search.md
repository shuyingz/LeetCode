## Breadth First Search

__1. Word Ladder__

```
https://leetcode.com/problems/word-ladder/
```

Given two words, beginWord and endWord, and a dictionary wordList, return the number of words in the shortest transformation sequence from beginWord to endWord, or 0 if no such sequence exists.

```
Example 1:

Input: beginWord = "hit", endWord = "cog", wordList = ["hot","dot","dog","lot","log","cog"]

Output: 5

Explanation: One shortest transformation sequence is "hit" -> "hot" -> "dot" -> "dog" -> cog", which is 5 words long.


Example 2:

Input: beginWord = "hit", endWord = "cog", wordList = ["hot","dot","dog","lot","log"]

Output: 0

Explanation: The endWord "cog" is not in wordList, therefore there is no valid transformation sequence.
```


__Pseudo Code Template:__

```
def _word_ladder(self, start, end, dict):
  # _create a queue and add start
  queue = collections.deque([start])

  # create an visited set for graph
  visited = set([start])

  distance = 0  # --> TO RETURN

  # _loop queue
  while queue:
    distance += 1
    for i in range(len(queue)):
      word = queue.popleft()  # _popleft staffs from queue

      if word == end:
        return distance

      ... if current word doesn't match end word, get all possible 'next words', loop them and lookup if it's in dict or visited

      if 'next word' is in dict:
        queue.append(next_word)
        visited.append(next_word)

  return 0  # return 0 for not found

```

__2. Number of Islands__

```
https://leetcode.com/problems/number-of-islands/
```

Given an `m x n` 2D binary grid grid which represents a map of `'1's` (land) and `'0's` (water), return the number of islands.

An island is surrounded by water and is formed by connecting adjacent lands horizontally or vertically. You may assume all four edges of the grid are all surrounded by water.

```
Example 1:
Input:

grid = [
 ["1","1","1","1","0"],
 ["1","1","0","1","0"],
 ["1","1","0","0","0"],
 ["0","0","0","0","0"]
]
Output: 1


Example 2:
Input:

grid = [
 ["1","1","0","0","0"],
 ["1","1","0","0","0"],
 ["0","0","1","0","0"],
 ["0","0","0","1","1"]
]
Output: 3
```

__Pseudo Code Template:__

```

```