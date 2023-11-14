# 2011 Final Value of Variable After Performing Operations - 
There is a programming language with only four operations and one variable X:

++X and X++ increments the value of the variable X by 1.
--X and X-- decrements the value of the variable X by 1.
Initially, the value of X is 0.

Given an array of strings operations containing a list of operations, return the final value of X after performing all the operations.

Example 1:

Input: operations = ["--X","X++","X++"]
Output: 1
Explanation: The operations are performed as follows:
Initially, X = 0.
--X: X is decremented by 1, X =  0 - 1 = -1.
X++: X is incremented by 1, X = -1 + 1 =  0.
X++: X is incremented by 1, X =  0 + 1 =  1.


```python
# create a function 
#function that calculates the final value of a variable x
def finalOperations (perations):   
# given intinal value of x is 0    
    x = 0
    # operations are represented as strings in a list .
    Operations = ["--X", "X++", "X++"]
# using for loop condition we will find out operation that either increments (++X or X++) or decrements (--X or X--) the value of x.
    for op in finalOperations: 
        if "++X" == op:  # increments x by 1 (due to the  X++)
            x += 1
       
        elif "--X" == op: # decrements x by 1 (due to the--X)
            x -= 1
        
        elif "X++" == op: #increments x by 1 (due to the X++)
            x += 1

    return x
# testing the function
Operations = ["--X", "X++", "X++"]

print(result)

```

    1
    

Example 2:

Input: operations = ["++X","++X","X++"]
Output: 3
Explanation: The operations are performed as follows:
Initially, X = 0.
++X: X is incremented by 1, X = 0 + 1 = 1.
++X: X is incremented by 1, X = 1 + 1 = 2.
X++: X is incremented by 1, X = 2 + 1 = 3.


```python
# create a function 
#function that calculates the final value of a variable x as per operation
def finalOperations(operations):
   # intinal value of x is 0  
    X = 0
    operations = ["++X","++X","X++"]
    for operation in operations:
        if operation == '++X' or operation == 'X++':  #The operations ++X and X++ increment the value of X by 1
            X += 1
        elif operation == '--X' or operation == 'X--': #the operations --X and X-- decrement the value of X by 1
            X -= 1
    return X


operations = ["++X","++X","X++"]
# ++X: X is incremented by 1. Initially, X was 0, so now X = 0 + 1 = 1.
# ++X: X is incremented by 1 again. Now, X = 1 + 1 = 2.
# X++: X is incremented by 1 once more. Now, X = 2 + 1 = 3.
print(finalOperations(operations)) 

```

    3
    

Example 3:

Input: operations = ["X++","++X","--X","X--"]
Output: 0
Explanation: The operations are performed as follows:
Initially, X = 0.
X++: X is incremented by 1, X = 0 + 1 = 1.
++X: X is incremented by 1, X = 1 + 1 = 2.
--X: X is decremented by 1, X = 2 - 1 = 1.
X--: X is decremented by 1, X = 1 - 1 = 0.


```python

# create a function 
#function that calculates the final value of a variable x as per operation
def finalOperations(operations):
   # intinal value of x is 0  
    X = 0
    operations = ["X++","++X","--X","X--"]
    for operation in operations:
        if operation == '++X' or operation == 'X++':  #The operations ++X and X++ increment the value of X by 1
            X += 1
        elif operation == '--X' or operation == 'X--': #the operations --X and X-- decrement the value of X by 1
            X -= 1
    return X


operations = ["X++","++X","--X","X--"]
# ++X: X is incremented by 1. Initially, X was 0, so now X = 0 + 1 = 1.
# ++X: X is incremented by 1 again. Now, X = 1 + 1 = 2.
# X--: X is decremented by 1 once more. Now, X = 2 - 1 = 1.
# --X: X is decremented by 1 once more. Now, X = 1 - 1 = 0.
print(finalOperations(operations)) 

```

    0
    

# 2006 Count Number of Pairs With Absolute Difference
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.


Example 1:

Input: nums = [1,2,2,1], k = 1
Output: 4
Explanation: The pairs with an absolute difference of 1 are:
- [1,2,2,1]
- [1,2,2,1]
- [1,2,2,1]
- [1,2,2,1]


```python
#create the function count_pairs(nums, k) is designed to count the number of pairs

def count_pairs(nums, k):
# import the counter from collection
    from collections import Counter
    count = Counter(nums)
    result = 0
    for num in count:
        if k > 0:
            if num + k in count:
                result += count[num] * count[num + k]
        elif k == 0:
            result += count[num] * (count[num] - 1) // 2
    return result

nums = [1,2,2,1]
k = 1
print(count_pairs(nums, k))  
```

    4
    

Example 2:

Input: nums = [1,3], k = 3
Output: 0
Explanation: There are no pairs with an absolute difference of 3.


```python
def count_pairs(nums, k):
    count = 0
    for i in range(len(nums)):
        for j in range(i+1, len(nums)):
            if abs(nums[i] - nums[j]) == k:
                count += 1
    return count


nums = [1,3]
k = 3
print(count_pairs(nums, k))
```

    0
    

Example 3:

Input: nums = [3,2,1,5,4], k = 2
Output: 3
Explanation: The pairs with an absolute difference of 2 are:
- [3,2,1,5,4]
- [3,2,1,5,4]
- [3,2,1,5,4]
 


```python
def count_pairs(nums, k):
    count = 0
    nums.sort()
    i = 0
    j = 1
    while j < len(nums):
        diff = nums[j] - nums[i]
        if diff < k:
            j += 1
        elif diff > k:
            i += 1
        else:
            count += 1
            i += 1
            j += 1
    return count

nums = [3,2,1,5,4]
k = 2
print(count_pairs(nums, k)) 

```

    3
    

# 1929 Concatenation of Array 


Given an integer array nums of length n, you want to create an array ans of length 2n where ans[i] == nums[i] and ans[i + n] == nums[i] for 0 <= i < n (0-indexed).

Specifically, ans is the concatenation of two nums arrays.

Return the array ans.

 

Example 1:

Input: nums = [1,2,1]
Output: [1,2,1,1,2,1]
Explanation: The array ans is formed as follows:
- ans = [nums[0],nums[1],nums[2],nums[0],nums[1],nums[2]]
- ans = [1,2,1,1,2,1]


```python
def concatenate(nums):
    
    ans = nums + nums
    return ans


nums = [1, 2, 1]
result = concatenate(nums)
print(result)

```

    [1, 2, 1, 1, 2, 1]
    

Example 2:

Input: nums = [1,3,2,1]
Output: [1,3,2,1,1,3,2,1]
Explanation: The array ans is formed as follows:
- ans = [nums[0],nums[1],nums[2],nums[3],nums[0],nums[1],nums[2],nums[3]]
- ans = [1,3,2,1,1,3,2,1]


```python
def concatenate(nums):
    ans = nums + nums
    return ans

nums = [1, 3, 2, 1]
result = concatenate(nums)
print(result)

```

    [1, 3, 2, 1, 1, 3, 2, 1]
    

# 1921
You are playing a video game where you are defending your city from a group of n monsters. You are given a 0-indexed integer array dist of size n, where dist[i] is the initial distance in kilometers of the ith monster from the city.

The monsters walk toward the city at a constant speed. The speed of each monster is given to you in an integer array speed of size n, where speed[i] is the speed of the ith monster in kilometers per minute.

You have a weapon that, once fully charged, can eliminate a single monster. However, the weapon takes one minute to charge. The weapon is fully charged at the very start.

You lose when any monster reaches your city. If a monster reaches the city at the exact moment the weapon is fully charged, it counts as a loss, and the game ends before you can use your weapon.

Return the maximum number of monsters that you can eliminate before you lose, or n if you can eliminate all the monsters before they reach the city.

 

Example 1:

Input: dist = [1,3,4], speed = [1,1,1]
Output: 3
Explanation:
In the beginning, the distances of the monsters are [1,3,4]. You eliminate the first monster.
After a minute, the distances of the monsters are [X,2,3]. You eliminate the second monster.
After a minute, the distances of the monsters are [X,X,2]. You eliminate the third monster.
All 3 monsters can be eliminated.




```python
from typing import List
def eliminateMaximum(self, dist: List[int], speed: List[int]) -> int:
        n = len(dist)
        arrivalTime = [(d - 1) // s for d, s in zip(dist, speed)]

       
        arrivalTime.sort()

        for i in range(n):
            if i > arrivalTime[i]:
                return i

        return n
print(result)
```

    2
    








```python

```


```python

```


```python

```


```python

```
