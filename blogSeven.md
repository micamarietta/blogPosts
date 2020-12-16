# Blog No. 7
## Normal Forms and Confluence

Now that we are familiar with the concept of an ARS, using input and rules within an ARS to observe the manipulation of data, and the meaning behind the relationship that -> creates, we can now further characterize various ARS's. By using the term "characterize", I mean that we can use terms that will make describing patterns within our ARS and set of rules much easier. With this we can take a look at confluence and normal forms.

*This blog post is intended to be supplemental to our practice in class during the lectures regarding confluence and normal forms to provide for simple explanations that may provide for greater overall understanding.

### Normal Forms

To understand normal forms, we first need to understand the concept of something being **reducible**. Something reducible in an ARS follows a similar definition to fractions being reduced, or mathematical expressions being simplified. As Professor Kurz mentioned in his blog, element */a/* is reducible if there is */b/* such that */a -> b /*.

With this, we can now understand what normal forms are. If an element of an ARS (a for example) is a **normal form**, then it is not reducible, or it is **irreducible**. Again, one analogy I think of is fractions and simplifying fractions. For example, if you think about normal forms in terms of the analogy, 2 is the "normal form" of the fraction 4/2, since it cannot be reduced any further.

The term normal form can be applicable to both sides of a rule, like a -> b. For example:

- a has normal form b if a reduces to b and b is a normal form
-b is a normal form of a if a reduces to b and b is a normal form

These examples illustrate that our term is interchangeable, and it is important to read things carefully when interpreting sentences like these into rules of an ARS.

#### Unique Normal Form

**Unique normal form** is a special case where an element has **exactly** one normal form. Let's take a look at an example:

Set T = {a,b,c,d,e}

a -> b <br/>
a -> c <br/>
d -> e <br/>

With this, we can see that **d has unique normal form e** while **a has normal forms b and c, but not unique normal form**.

I feel that normal forms are not fairly difficult, but to practice, I recommend creating your own ARS's with different sets and rules, and just looking over them to determine what the normal form or unique normal form of each element of your ARS is.

### Confluence
Confluence can be described as a property of our ARS. An ARS is said to be **confluent** if for all elements of our set, the paths we take to manipulate different elements (for example a -> b or bb -> bcbc) are all joining at some common ancestor. For example:

Let's begin with a set T.

T = {a,b,c,d}

Rules: <br/>
a -> b <br/>
b -> c <br/>
d -> [] <br/>

Our set is confluent. No matter where you start with any input, no rules are overlapping. 

Our set can obviously be more complicated. In order to check for confluence of a more complicated set, we can try out a series of inputs that we suspect may have different reductions.

Let's say we have a set S.

S = {a,b,c,d}

Rules: <br/>
Rules:
a -> bc <br/>
b -> a <br/>
ba -> bc <br/>
ab -> bb <br/>
bc -> c <br/>
aa -> <br/>

Our set is **not** confluent. While the inputs a, b, ba, and bc all reduce to the common ancestor c, ab and aa reduce to cc and [] respectively.

For more practice, it is helpful to create your own rules and just go through determining normal forms as well as confluence.
