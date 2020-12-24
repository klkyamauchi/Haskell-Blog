# Entry #7 - Introduction to Lambda Calculus

#### What is Lambda Calculus?
Lambda Calculus is a mathematical model or "language" that helps us understand computation. It can model any computation done by a computer, which is pretty powerful. 

#### Components of Lambda Calculus
 Lambda calculus is made up three components: variables, application, and abstraction.  

 **variables**: can be defined as x, y, z, etc. 

 **abstraction**: defined by a function (lambda), the function's arguments followed by a dot, and what the function returns.  
 
For example, the function $f(x) = x)$ can be written as $λx.x $ in lambda calculus. 

These abstractions can also be nested. We see the following in lambda calculus: $λx.λy.xy$ is equivalent to $f(x,y) = xy$. 

**application**: when a function is applied to an argument. Let $g$ and $f$ be programs, then $fg$ is a program in which the function $f$ is being applied to the argument $g$. 

#### Rules of Lambda Calculus

Lambda calculus can get pretty messy, so there are more rules when it comes to adding and dropping parenthesis that can increase legibility. 

1. **Application associates to the left** 
    For example, $abc$ parses to $((ab)c)$ and $abcd$ would parce to $(((ab)c)d)$. 
2. **Application has higher precedence than abstraction**
 Whenever you see nested abstractions in lambda calculus, the parenthesis go to the right most term. For example, in the following: $λx.λy.x$ would be parsed to $λx.(λy.x)$ for the function $f(x,y) = x$. 

 #### Helpful Resources
 I personally struggled a lot with understanding where to add parentheses and where to drop them. I remember watching videos my professor posted over and over again to try and get the hang of it. One video I found on Youtube I found particularly helpful when first getting started with lambda calculus can be found [here](https://www.youtube.com/watch?v=d0yEXKas8xE). Here are the videos my professor created that help walked me through some examples with parsing lambda calculus. This is the [first](https://www.youtube.com/watch?v=eYstx7uuE6c&feature=youtu.be) of them, but I found the [second](https://www.youtube.com/watch?v=yls1NEUlzZA&feature=youtu.be) one particularly helpful. 

This is another [helpful page](http://dev.stephendiehl.com/fun/lambda_calculus.html) that I found that goes through a full walkthrough with lambda calculus. It goes through topics such as substitution, reduction, recursion, and makes helpful references to Haskell itself. 