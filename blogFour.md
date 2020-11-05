# Blog No. 4
## A Look at Abstract and Concrete Syntax

Abstract and concrete syntax are important concepts we have been learning about in class. In this blog, the aim is to define abstract and concrete syntax in simple terms. This will enable further understanding when implementing a calculator in Haskell (assignment 1) and for becoming accustomed to writing in the Haskell syntax.


### Abstract Syntax

Abstract syntax of data is the structure described as a data type. When dealing with abstract syntax, we want to ask ourselves **what are the significant parts of the expression?** This syntax is often illustrated within an abstract syntax tree. In the tree, each node denotes a specific object or construct within the program:

**Plus** (from the cse.chalmers website in the notes)

          plus
        /      \
       /        \
      6          8

**Times**

          times
        /       \
       /         \
      6           8


Every implementation of a programming language uses an abstract syntax. This means that the abstract syntax is pat of the definition of a specific implementation like a compiler of a language.


### Concrete Syntax

Concrete syntax of data is defining how the language of the abstract syntax is displayed and edited. When thinking of concrete syntax, we want to ask **what does the expression look like?** With concrete syntax, we can think of an example where the *same* expression can look different when being presented differently. Here's an example from the abstract trees from above:

**Plus** (from the cse.chalmers website in the notes)

6 + 8            --infix

(+ 6 8)          --prefix

(6 8 +)          --postfix

sum of 6 and 8        --english

adding 6 and 8 together        --english

**Times**

6 * 8            --infix

(* 6 8)          --prefix

(6 8 *)          --postfix

product of 6 and 8        --english

multiplying 6 and 8 together        --english

performing 6 times 8         --english


With this, we can see that concrete syntax illustrates that we can present the same expression in multiple ways. Although some of these presentations look odd, we can use concrete syntax to completely change the presentation of a language.

**Example Illustration: Concrete Syntax Impacting C++**

Imagine changing the syntax of adding in C++. This is an example of changing its concrete syntax.

For printing 6 + 8 in C++, it would look like this:

cout << 6 + 8 << endl;

If we were to change our presentation of adding to be a prefix, adding in C++ would look like this:

cout << (+ 6 8) << endl;

We could do this with anything else in C++ that is not necessarily even computational (example: concatenation, if statements, comparison operators, etc).

I felt that using this as an example really helped me understand what concrete syntax actually is, and how familiar we are with the concept of it already through various coding classes.
