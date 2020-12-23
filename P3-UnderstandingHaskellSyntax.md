# Entry #3 - Understanding Haskell Syntax

Personally, I find that one of the most daunting things when learning a new language is the new syntax that comes along with it. With the imperative languages that I have learned previously, the transition from Python to Java to C++ to C was not all too terrible. The biggest jump was definitely from Python to Java, but after that the differences became minute between the next few. 

With Haskell however, seeing the syntax of a functional language for the first time definitely intimdated me. Just the thought of starting something completely new was a task in and of itself. However, once I got started on the first assignment, things went pretty smoothly. Starting is always the hardest part of a task, but within completing a few functions, completing my first assignment didn't seem all too bad. 

## Back to The Basics

My hope is that this post will provide all that is necessary to grasp the basics of Haskell. Whenever I learn a new language, I like to refer to a "cheat sheet" that outlines types, arithmetic, built-in functions, etc. until it all becomes second nature. Hopefully this post can act as your cheat sheet! 

#### Comments
<pre><code> -- comments are written with the preceded double dashes
</code></pre>

#### Types
<pre><code>integer :: Int
integer = 2

str :: String
str = "Hello World!"

character :: Char
character = "K"

tumple :: (Int, String, Char)
tuple = (integer, str, character)

list = [1, 2, 3, 4, 5]
</code></pre>

#### Arithmetic
Haskell has all the basic arithmetic functions and follows the same precedence rules as other programming languages. We can also set our own precedence using parentheses. 
<pre><code>1 + 2     -- = 3 Addition
3 * 4     -- = 12 Multiplication
6 - 5     -- = 1 Subraction
15 / 3    -- = 5 Division
16 % 9    -- = 1 Modular Arithmetic

(2*4) + 6   -- = 14
2 * 4 + 6   -- = 14
2 * (4+6)   -- = 20
</code></pre>

#### Boolean Algebra
<pre><code>&&     -- logical and
||     -- logical or
not    -- negation

True && False     -- False
True && True      -- True
False || True     -- True
not False         -- True
not (True && True)  -- False
</code></pre>

#### Equality
You can compare elements of the same type, just as in other programming languages but will run into an error when comparing elements of two different types. 
<pre><code>
9 == 9    -- True
3 == 4    -- False
1 /= 1    -- False
6 /= 7    -- True
"hello" == "Hello!"   -- False
"hello" == "hello"    -- True
</code></pre>

#### Function Definitions 
Functions are defined in Haskell first by name then arguments and return type, separated by two colons "::"
This declaration is followed by the function body. 

In the following function, plusOne, one argument (an integer) is passed in and the function will return that integer incremented by one!
<pre><code>plusOne :: Int -> Int
plusOne int = int + 1
</code></pre>

### References
Listed below are the references I used to create this page and what helped me learn the basics of Haskell!
- http://learnyouahaskell.com/starting-out
- https://andrew.gibiansky.com/blog/haskell/haskell-syntax/
 


