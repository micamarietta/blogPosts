# Blog No. 2
## Recursion & the Fibonacci Sequence (Pt 1)

Recursion is defined as the repeated application of a procedure or definition. My initial understanding of recursion was through coding, where it was ideal for solving problems that can be broken down into small repetitive processes. Sometimes it can be somewhat difficult to think of a way to simplify a problem into a few recursive lines to write. However, I think that with a strong mathematical background of what exactly recursion is.

### Fibonacci Sequence Example

As mentioned through lecture, when applying recursion to a program, we first want to understand the mathematical definition of recursion. This is often shown through mathematical equations, and a great example is one we used in class- the Fibonacci sequence.

The Fibonacci sequence is a set of numbers that starts with a one or a zero, followed by a one, and proceeds based on the rule that each number (called a Fibonacci number) is equal to the sum of the preceding two numbers (Rouse, techtarget.com)

The Fibonacci sequence can be broken up into sub-processes:

fib(0) = 0
fib(1) = 1
fib(n+2) = fib(n) + fib(n+1)  

One way we can show this is through a tree that illustrates the sub processes of the sequence:

#### Activity: Creating a Fibonacci tree diagram

                    fib(6)
                      |
                      +
                /           \
            fib(4)        fib(5)
               |            |
               +            +
            /     \      /     \
        fib(2)  fib(3) fib(3)  fib(4)
          |       \
          +        \
      /     \        +
  fib(0)  fib(1)   /   \
                fib(1) fib(2)

*(Did not expand upon fib(3) and fib(4) on the right hand side, because they are defined on the left)

With knowing that fib(0) = 0 and fib(1) = 1, we can use these as our base cases for our problem to be broken down into.
Therefore, fib(6) = 8.

#### Activity: Implementing a recursive Fibonacci program in Python and Java

We are able to use this mathematical definition and recursive logic to implement a simple Fibonacci sequence function in various programming languages. Let's implement them in Python and Java before moving onto Haskell.

##### Note: I chose to implement this in both python and Java because I am comfortable with the syntax of these two languages. With comfortability with the syntax, I felt that I could have a greater understanding of implementing recursive functions in Haskell.

By implementing this function in Python and Java, we can compare them, and observe if recursion significantly changes through use of different syntax and interpreted and compiled languages.


**Python Fibonacci function:**

def fib(n):

  //our base cases (n = 0 OR n = 1)
  //could also be "if (n <= 1)"
  if(n<2):
    return n

  //our recursive call
  else:
    return(fib(n-1)+fib(n-2))

**Java Fibonacci function:**

public static int fib(int n){

  //base case
  if(n < 2) return n;

  //recursive call
  else{
    return (fib(n-1) + fib(n-2))
  }
}

It was fairly easy to see that the only major difference between the Python and Java fib functions is different syntax. Both were very simple to implement, and the only real changes to make were that of syntax (as expected).

I thought this was helpful in that it showed me this will be easier to implement in Haskell than I thought. For me, with Haskell's very different syntax (in comparison to Python and Java), it seemed challenging for me to write a recursive Haskell function. However, doing this exercise helped me to see that the only real hurdle to tackle is the Haskell syntax.

In my next blog, I will continue to talk about recursion, but instead implementing recursion in Haskell. 
