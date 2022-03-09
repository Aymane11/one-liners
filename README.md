# one-liners

A list of my daily used Python one liners (especially on [CodinGame's Clash of Code](https://www.codingame.com/multiplayer/clashofcode))

---

## User Input

### Get two numbers from space-separated user input

```python
# example: 1 2 -> x = 1, y = 2
x,y = map(int,input().split()) # can replace int by float
```

### Get list of numbers from space-separated user input

```python
# example: 1 2 3 4 5 -> nums = [1, 2, 3, 4, 5]
nums = list(map(int,input().split())) # can replace int by float
```

### Get list of lists of numbers (matrix) from user input

```python
# example:
# 3         # size of the matrix
# 1 2 3  ->  matrix = [[1, 2, 3],
# 4 5 6                [4, 5, 6],
# 7 8 9                [7, 8, 9]]
matrix = [list(map(int,input().split())) for _ in range(int(input()))] # can replace int by float
```

### Other cases

```python
# example: 1 2 3 -> x = 1, y = 3
x,_,y = map(int,input().split()) # we don't care about the second number

# example: 1 2 3 4 5 -> x = 1, y = 5
x,*_,y = map(int,input().split()) # we only care about the first and last numbers
```

## Output

### Print a list of numbers

```python
# example: nums = [1, 2, 3, 4, 5] -> print 1 2 3 4 5
print(*nums) # can replace *nums
```

### Print a matrix (list of lists)

```python
# example:
# matrix = [[1, 2, 3], -> 1 2 3
#           [4, 5, 6],    4 5 6
#           [7, 8, 9]]    7 8 9
print('\n'.join(map(lambda x: ' '.join(map(str,x)), matrix)))
```

## Other

### Get distinct elements from an iterable (list, string ...) without changing order

```python
# example: nums = [4, 1, 2, 3, 1, 4, 3] -> nums = [4, 1, 2, 3]
# example: string = 'abacbad' -> string = ['a', 'b', 'c', 'd'] # can use join to get a string
distinct = list(dict.fromkeys(my_iterable).keys())
```
