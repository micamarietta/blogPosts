# Blog No. 6
## An intro to ARS's (ARS Blogs Pt. 1)

When initially going over the concept of an ARS, or **Abstract Reduction/Rewriting System**, I think I definitely over-complicated the idea of what ARS actually is. With this blog, I want to provide a brief intro and summary to the concept of an ARS and the concept of confluence that will be simple and easy to follow. I think this will be helpful for learning more concepts that relate to an ARS.

### An ARS

I think an **ARS** can be simply defined as a process where a set of rules transforms and manipulates data (https://www.encyclopedia.com/computing/dictionaries-thesauruses-pictures-and-press-releases/abstract-reduction-system). With this definition, I think it is easier to imagine an ARS. Here's one example of an ARS:

set T = {a, b, c}

Rules:
a -> b
b -> c
c ->

With this ARS, we can see that with our given rules, we would be able to break down input given, almost like a program would with a set of steps. For example, let's say **our input is a**.

**Things to keep in mind:**
  - we can only move from **left to right**. For example, with the rule a -> b, we cannot say that b -> a. Our rules are not interchangeable.
  - sometimes, there are multiple ways to convert our input data into our output data. There can also be alternate outputs that are generated based on the rules we are provided. **Illustrated in a later example with input 3**.

From our rules,

we know we can first reduce a to b using this rule:
a -> b

then from there, b can reduce to c, using the rule...
b -> c

and then c can reduce to an empty [] (or nothing) using the rule...
c ->

With this simple example, we were able to observe the basic state of the ARS, where we could use our set and our rules to transform our input data. Not too bad right? I definitely encourage anyone who wants to get more comfortable with the
concept of an ARS to try to write your own set of rules and test different inputs with your set of rules.

Now let's try a more difficult example...

set S = {a, b, c}

Rules:
a -> bc
b -> a
ba -> bc
ab -> bb
bc -> c
aa ->

With this set of rules, lets try a few different inputs:
**Input 1** = a
**Input 2** = bb
**Input 3** = abbc

#### Input 1:

a -> bc
bc -> c

because there is no rule that transforms c to another set of letters or letter, c is our ending point.

#### Input 2:

bb -> aa
aa -> bcbc
bcbc -> cc

cc is our ending point.

#### Input 3:

*This input is great at illustrating that there are many ways to convert our inputs using our set of rules and that
it is possible for us to have different outputs from the same input and same set of rules.

**Solution 1:**

abbc -> bbbc       ---- uses the rule ab -> bb
bbbc -> bbc
bbc -> aac
aac -> bcbcc
bcbcc -> ccc

ccc is our ending point.

**Solution 2:**

abbc -> bcbc       ---- uses the rule a -> bc
bcbc -> cc

cc is our ending point.


With using inputs and stepping through the logic of the rules of our ARS's, we were able to see the process that an ARS creates, almost illustrating the concept of the ARS like stepping through steps in code. We can analyze these ARS's for different things, inlcuding **confluence** and **termination**. In my next blogs, we will cover these concepts with more
ARS examples.
