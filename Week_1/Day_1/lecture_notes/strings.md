# Strings

Strings are texts. Thing of strings are words and characters. In Ruby a string is anything inside of quotes.

## Methods
* [Indexing ([])](#indexing)
* [String.downcase](#downcase)
* [String.upcase](#upcase)
* [String.index](#index)
* [String.slice](#slice)
* [String.length](#length)
* [`+` (concatenation)](#concat)
* ['!' (bang)](#bang)

### <a name="indexing">Indexing into Strings</a>

Indexing is the way we can grab specific characters out of a string. Indexing for strings starts at 0 and then increments by one depending on how many characters are in the string. To grab a character from the string we use the string and then square brackets with the index of the character between them.

```ruby
"Hello World"[0] # => H
"Hello World"[1] # => e
"Hello World"[2] # => l
"Hello World"[6] # => W
"Hello World"[8] # => r
```

Ruby also has the ability for negative indexing. Negative indexing is where we can put a negative number in between the square brackets and index from the end of the string.

```ruby
"Hello World"[-1] # => d
"Hello World"[-2] # => l
"Hello World"[-10] # => e
```

### <a name="downcase">Downcase</a>

What happens if we have a word that has some letters that are capitalized and we want all of the characters to be lowercase? In comes .downcase to save the day!

```ruby
"Hello World".downcase # => hello world
"ALL UPCASE!!!".downcase # => all upcase!!!
"WeIrD cAsE".downcase # => weird case
```

### <a name="downcase">Upcase</a>

Now we have a string that's all lowercase, but now we want it in all caps! Let's look to our friend .upcase!

```ruby
"Hello World".upcase # => HELLO WORD
"all downcase!!!".upcase # => ALL DOWNCASE!!!
"WeIrD cAsE".upcase # => WEIRD CASE
```

### <a name="index">Index</a>

Let's not confuse index with indexing into a string. We use the index method when we have an element and we want to find the index of that element in our string.

```ruby
"Hello World".index('e') # => 1
"Hello World".index('l') # => 2
"Dogs are cool".index('a') # => 5
"Skateboards".index('o') # => 6
```

What if we have a whole word that we want to find in the string? Our good friend index can still help! When given a more than one letter index returns the index where our word starts in the string.

```ruby
"Hello World".index('World') # => 6
"Hello World".index('ello') # => 1
"Dogs are cool".index('cool') # => 9
"Skateboards".index('rds') # => 8
```

What about the case where our letter or word doesn't exist in the string? When given an element that doesn't exist in the string index will return 'nil'. Index looks for an Exact match. If our string contains a lowercase 'a' and we look for an uppercase 'A', index will still return 'nil'.


```ruby
"Hello World".index('z') # => nil
"Hello World".index('E') # => nil
"Dogs are cool".index('Cats') # => nil
```

### <a name="slice">Slice</a>

What if we only want part of the string? Slice is the tool for the job! Slice when given one arguments will cut out the character in the string at that index.

```ruby
"Hello World".slice(1) # => 'e'
"Hello World".slice(2) # => 'l'
"Dogs are cool".slice(5) # => 'a'
"Skateboards".slice(6) # => 'o'
```

Slice can also a second optional argument. This number is how many letters to slice out of the string starting at the index of the first argument.

```ruby
"Hello World".slice(1, 3) # => 'ell'
"Hello World".slice(2, 6) # => 'llo Wo'
"Dogs are cool".slice(5, 8) # => 'are cool'
"Skateboards".slice(5, 6) # => 'boards'
```

We also can slice using square brackets and periods. Using square brackets requires 2 arguments and either 2 periods or 3 periods. When using square brackets the first argument is the start index and the second argument is the ending index.

When using 2 periods the ending index is included. When using 3 periods the ending index is not included.


```ruby
"Hello World"[1..3] # => 'ell'
"Hello World"[6..-1] # => 'World'
"Dogs are cool"[0...3] # => 'Dog'
"Skateboards"[2...5] # => 'ate'
```

### <a name="length">Length</a>

Length does exactly what we think it should do. Length returns how many characters are in the string.

```ruby
"Hello World".length # => 11
"Dogs are cool".length # => 13
"Skateboards".length # => 11
"Cat".length # => 3
```

### <a name="concat">`+` (concatenation)</a>

Concatenation (or concat) is a fancy word for taking 2 words and putting them together as one word. When concating 2 words in Ruby we can either use + or string1.concat(string2). The only difficulty is when concating 2 stings they are put together exactly how give them, no spaces are added.

```ruby
"Hello" + "World" # => "HelloWorld"
"Hello" + " World" # => "Hello World"
"Skate".concat("board") # => "Skateboard"
"#Yes We".concat(" Code") # => "#Yes We Code"
```

### <a name="bang">`!` (Bang!)</a>

Up to this point every method we've used is an immutable method. This means that they don't change the string that they're called on.

```ruby
str1 = "#Yes We Code"
str1.upcase
puts str1 # => "#Yes We Code"

str2 = "ALL CAPS!"
str2.downcase
puts str2 # => 'ALL CAPS!'
```

If we add `!` (or bang) to the end of the method name it becomes a mutable method. This means that the method does change the string that it's called on.

```ruby
str1 = "#Yes We Code"
str1.upcase!
puts str1 # => "#YES WE CODE"

str2 = "ALL CAPS!"
str2.slice!(0, 3)
puts str2 # => 'ALL'
```
