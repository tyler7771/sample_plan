## Problems Week 3 Day 4

Solve the problems! The problem is correct if each case prints out true.

```ruby
# Write a Dog class that has three methods. Dog.speak which prints  
# out "bark bark", Dog.give_toy(toy) which adds the toy to the  
# dog's toys, Dog.toys which returns all of the dog's toys.

class Dog
  # Put code here
end

dog = Dog.new
puts dog.bark == "bark bark"
dog.give_toy("Bone")
dog.toys == ["Bone"]
dog.give_toy("Ball")
dog.give_toy("Stuffed Animal")
dog.toys == ["Bone", "Ball", "Stuffed Animal"]
```
