## **Understanding Syntax by Implementing Functions**
Learning by doing!

### **Data Definitions**

For my first assignment, we were told to implement a basic calculator. To start off, we defined a data type for natural numbers as seen below. 

<pre><code> data NN = O | S NN 
</code></pre> 
* We are defining our natural number as either zero (O) or 1 (S) plus some other natural number 
* In this sense, our S's are like tally marks and we build numbers by concatenating them onto O. 

For example:
<pre><code> O         -- = 0
 S O       -- = 1 + 0 = 1
 (S (S O)) -- = 1 + 1 + 0 = 2
</code></pre>

and so on... Note that with numbers greater than 1, we separate the S's with parenthesis. 

### **Function Definitions**
For the next few functions below, I will give examples and outline my thought process while creating them through comments. 

<pre><code> -- addition
add :: NN -> NN -> NN     -- define the function 
add O n = n               -- base case: 0 + n = n
add (S n) m = S (add n m) -- recursive step</code></pre>

* In defining the function, we take in two inputs (NN -> NN) and produce another natural number, -> NN
* In the recursive step, we are pulling out an S and calling the function add again to continue pulling out and concatenating an S onto the result until the base case is reached. 

<pre><code> -- multiplication
mult :: NN -> NN -> NN           -- define the function
mult O n = O                     -- base case: 0 * n = 0
mult (S O) n = n                 -- base case: 1 * n = n
mult (S n) m = add m (mult n m)  -- recursive step </code></pre>
* In this recursive step, we want to concatenate an S onto the resulting number (S n) amount of times. 
* Everytime we concatenate (add) we decrement the amount of times we have to add m amount to the result. 

<pre><code> -- subtraction 
subtr :: NN -> NN -> NN        -- define the function
subtr O n = O                  -- base case: 0 - n = 0 (natural numbers only)
subtr n O = n                  -- base case: n - 0 = n
subtr (S n) (S m) = subtr n m  -- recursive step </code></pre>
* In this recursive step, we continue to subtract n and m (decrementing by 1 (S) each time) until the base cases are hit. 
* m will become of size 0 or both n and m are of the same size and result in 0. 


 I found it helpful to think of the steps we take/how we know when to end when preforming simple arithmetic (as in grade school) to figure out the base and recursive steps of the Haskell functions. 



