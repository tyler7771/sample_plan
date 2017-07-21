# Strings

Strings are texts. Thing of strings are words and characters. In Ruby a string is anything inside of quotes.



## Methods
* [Indexing ([])](#indexing)
* <a name="downcase">String.downcase</a>
* <a name="upcase">String.upcase</a>
* <a name="index">String.index</a>
* <a name="slice">String.slice</a>
* <a name="length">String.length</a>
* <a name="concat">`+` (concatenation)</a>

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
