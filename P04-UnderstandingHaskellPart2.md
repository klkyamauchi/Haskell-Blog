# Entry #4 - Introduction to Lists

Lists in Haskell contain one type, meaning you are unable to put elements of the type Integer in the same list as elements of the type String. Haskell, unlike other programming languages you may be accustomed to can also have *infinite* lists, which can help cut computation time.

##### Some examples of possible lists in Haskell:
<pre><code>strings = ["hello", "world", "what", "is", "good?"]
nums = [1,2,3,4,5]
chars = ["h", "e", "l", "l", "o"]
</code></pre>

##### More Possible Lists:
In Haskell, much like in discrete math with sets and the empty set, we can have an empty list, a list containing the empty list, and a list of empty lists.

<pre><code>[]              -- empty list  
[[]]            -- an empty list containing an empty list
[[], [], []]    -- a list of empty lists
</code></pre>

#### List Operators
: will add an element to the front of a list  
++ will combine two lists together  
!! will obtain an element at the given index (Note: Haskell uses 0 based indexing)  

<pre><code>4:[1,2,3] -- becomes the following line
[4,1,2,3]

["h","e","l"] ++ ["l", "o", "!"] -- becomes the following line
"hello!"      -- note that a list of chars is simply just a string

[0, 1, 2, 3, 4] !! 1    -- becomes the following line
1

"hello world!" !! 3     -- becomes the following line
l 
</code></pre>

#### Haskell's List Functions
Just a taste of some of the basic  list functions Haskell has to offer: 

**head** - returns the first element of a given list  
**tail** - returns everyting after the head of a given list  
**last** - returns the last element of a given list  
**init** - returns all but the last element of a given list  
**length** - returns the length of a given list  

<pre><code>head [5,4,3,2,1]     -- returns 5
tail [5,4,3,2,1]     -- returns [4,3,2,1]     
last [5,4,3,2,1]     -- returns 1
init [5,4,3,2,1]     -- returns [5,4,3,2]
length [5,4,3,2,1]   -- retuns 5
</code></pre>

### References
See the referneces in the [last post](https://github.com/klkyamauchi/Haskell-Blog/blob/main/P3-UnderstandingHaskellSyntax.md) for more in depth discussion on lists in Haskell! 