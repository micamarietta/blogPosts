# Blog No. 3
## Recursion & Implementing Recursion in Haskell (Pt 2)

In my previous post, I discussed recursion, the Fibonacci sequence, and wrote two functions (one in Python and one in Java) that computed the Fibonacci sequence recursively.

With this, I was able to get a good foundation with the concept of recursion before creating recursive Haskell functions.



### Haskell Fibonacci Sequence Program

Let's start with using the Fibonacci sequence for our first recursive Haskell function. I also find that analyzing each line helps me understand the Haskell syntax.

*Fibonacci Program:

fib 0 = 0
fib 1 = 1
fib n = fib(n-1) + fib(n-2)

From writing this in Haskell, we can see how similar it was to the Python and Java Fibonacci sequence functions (maybe even simpler with the Haskell syntax).

**On line 14**, we define our first base case, or the lowest subproblem in our function that we need to define. When we complete a recursive call in our function, it will eventually break down into our base case.

**On line 15**, we define our second base case.

Lastly, **on line 16**, we define our recursive call. In Haskell, our call first includes the name of our function followed by an undefined variable "n", that will be filled with any positive number. From there, we call the function again like we did in Python and Java.

When running this function, I tested out several values in my command prompt:

fib(6)
fib(8)
fib(10)

Afterwards, the command prompt returned these values for each of the functions:

8
21
55


----------------------------------------------------------


With this, I thought it would be interesting to try some different recursive functions in Haskell (that aren't the Fibonacci sequence :))

I remember doing a lot of recursion in Python and Java with lists and arrays, computing length, removing each element, etc. Here, I want to show a **Haskell function  that indicates the length of a list**.


### Haskell List Length Program

//indicates that our function will take in a list and output and integer
length :: [n] -> Int

//base case
length [] = 0

//recursive call
length(x:xs) = 1 + length xs


This function will keep adding one to our length integer that is returned until we reach our base case, an empty list.

To test the function, I entered the following in command prompt:

length [1,2,3,4,5]

In return, the function outputted this, correctly giving us the length of our list:

5

We haven't yet implemented lists or used lists in Haskell, but this example illustrates that even with different data types like lists, the recursive Haskell logic is very simple.
