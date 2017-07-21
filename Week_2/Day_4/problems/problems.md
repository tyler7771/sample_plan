## Problems Week 2 Day 4

### Debugging Problems

Debugg the problems.

```ruby
def first_one_hundred
  idx = 0
  nums = []

  while idx <= 100
    nums << idx
    idx ++ 1
  end
end

puts first_one_hundred
```


### Coding Problems

Solve the problems! The problem is correct if each case prints out true.

```ruby
# Write a method valley_finder(arr) that takes an array of numbers. Return an array of valley indexes.

# A valley is when a number is less than numbers on either side of it. If the number is the first number it's less than the number on it's right. If the number is the last number it's less than the number on it's left.

# Hint can be solved with one loop

def two_dimensional_sum(arr)
  # Put code here
end

puts valley_finder([5, 6, 2, 3, 1]) == [2, 4]
puts valley_finder([2, 1, 8, 10, -9, -2, 7]) == [1, 4]
puts valley_finder([1, 4, 7, 20, 22, 8]) == [5]
```
