# Blog No. 5
## A Brief Introduction to Lambda Calculus

When first hearing the words "lambda calculus", I was a little concerned that the topic would be very difficult and dauting (most likely because of the word "calculus"). This blog is intended to simplify the concept of lambda calculus to provide for easy understanding and therefore easier implementation.

### The Three Programming Constructs

As mentioned within the lecture notes, these are the only three programming constructs of lambda calculus, **Abstraction, Application, and Variables**.

#### Abstraction
Abstraction was the concept that was somewhat confusing to me when initially learning about lambda calculus. I think it is helpful to initially think of the abstraction concept as an expression or a function (other names for abstraction in this context). The example expression we used was:

λx.e

where **e** is a program and **x** is a variable.

The **λ** means "function".

**Comparison to a javascript function**

**Lambda calculus:** λx.e

**Javascript:** function(x) {return x; }

With this, we see that our lambda calculus abstraction, or expression, is basically what we think of when we declare a function in another language like javascript, just with different concrete syntax.

#### Application
I think the example in the notes is a great way to illustrate the application concept:

e1e2

where **e1** and **e2** are both programs, the function e1 is applied to our argument e2.

For more examples of the application concept of lambda calculus I thought this website was very helpful: http://cs242.stanford.edu/f19/lectures/02-1-lambda-calculus#:~:text=The%20lambda%20calculus%20is%20a,That's%20it!

**Example from Site:**

One example in particular that I thought helped in my understanding of application of lambda calculus was when they mentioned being able to **nest functions** as we do commonly in other languages:

λ x . λ y . (x y)

This can be read as a function that takes an input x, then returns a function that takes an input y, then calls function c with the argument y.

While this is a more complicated example, it illustrates that this is similar to other programming languages. To delve further into the example, this is what the above function would look like in javascript:

function(x){
  return function(y){
    return(xy);
  }
}

The only difference that is really present is again the concrete syntax.

#### Variables
And lastly, we have variables. The variables in lambda calculus act and are presented like any other variables you would see in math or computer science, so I don't feel that this needs much explanation.
