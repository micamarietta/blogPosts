# Blog No. 8
## Termination

With more comfortability with the concept of an ARS as well as confluence and normal forms, **termination** is a very significant and important process to understand.

We can begin with a basic definition of termination. Termination is simply "the act of bringing something to an end". I'm sure in coding classes or math classes, this subject has been brought up maybe when seeing when a while or for loop ends or **terminates**, or determining when a set of numbers ends or **terminates**. In considering termination within an ARS, we really aren't changing the definition of termination that we already know.

As Professor Kurz mentions, termination is something that is really important to prove, especially within programs. Programmers rarely ever want an infinite loop to run within code, and to ensure an infinite loop is not created, we must ensure that our logic eventually terminates.

Let's get into **how we can prove this in an ARS**. I think this is easiest using a concrete example. (For a general example using the term ϕ refer to Professor Kurz's lecture notes for termination)

Suppose we have an **ARS A**.

Our ARS, per usual, has a series of rules:

Rules:
a -> bb <br/>
a -> b <br/>
ba -> b <br/>
ab -> bb <br/>


In order to determine whether our ARS terminates, we can look at our rules and determine a **measure function**. If there is a function or relation within the rules that is consistent (aka a measure function), then we can conclude that **our ARS terminates**.

There are a few ways that Dr. Kurz laid out to elegantly create a measure function, but there is one strategy that I use consistently that I think is the easiest way to prove termination.

In our current ARS, A, we can create a measure function by "assigning" or mapping **a -> 1 and b -> 2**. We can consider our rules in decimal notation. With this, we can edit our rules:

Rules:
a -> bb <br/>
1 -> 22 <br/>

a -> b <br/>
1 -> 2 <br/>

b -> ba <br/>
2 -> 21 <br/>

ab -> bb <br/>
12 -> 22 <br/>

With this, we can see a pattern in our rules. The left side **is always less than the right side**. This can be our measure function:

Rules:
a -> bb <br/>
1 < 22 <br/>

a -> b <br/>
1 < 2 <br/>

b -> ba <br/>
2 < 21 <br/>

ab -> bb <br/>
12 < 22 <br/>

With this, because our measure function fulfills every rule in our ARS, our ARS is **terminating**.

For more practice with termination, it is helpful to determine whether different sets are terminating and determine measure rules for various ARS's.

To expand upon the topic, I thought the mention of the Turing system in regard to termination was really interesting. Here is a link to a paper about termination that uses the Turing system as the proof to a theorem: http://www.cs.tau.ac.il/~nachumd/papers/termination.pdf. This is the basic idea:

The theorem basically states that it cannot be determined whether a rewrite system is terminating, even with only two rules.

The Turing machines can be simulated by rewrite systems. Within any Turing machine, there is a two rule system that terminates for all initial terms iff the machine halts for any input tapes. It cannot be determined whether the system is halting uniformly and consistently, so therefore it can't be determined whether it is terminating or not.

The rest of the paper goes into the details within the terminating system to reinforce the theorem that an ARS cannot truly be concluded as terminating or non-terminating.

While this isn't directly related to learning termination in an ARS for the sake of the course, I think it still helps to get a good grasp on the concept of termination, almost as if you are learning a math theorem that aids with later computation.
