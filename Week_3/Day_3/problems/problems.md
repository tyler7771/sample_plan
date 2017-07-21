## Problems Week 3 Day 3

Solve the problems! The problem is correct if each case prints out true.

```ruby
# Write a method my_map(arr, &proc) that takes an array and a proc.  
# my_map returns a new array where each element is the element in  
# that index from the original array with the proc called on it.

class Array
  def my_map(&prc)
    # Put code here
  end
end

puts [1, 2, 3].my_map { |x| x * 3 } == [3, 6, 9]
puts [2, 4, 6].my_map { |x| x * 10 } == [20, 40, 60]
puts [1, 3, 5].my_map { |x| x + 5 } == [6, 8, 10]
```
