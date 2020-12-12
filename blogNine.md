# Blog No. 9
## Invariants

Invariants are a topic that, at first, I had a hard time understanding the concept of. However, with more experience and practice with working with them, the concept became fairly straightforward and something that is one of the first things I notice when looking at an ARS.

I like to think of an **invariant** simply as a condition that is true before and after an expression. We can determine a multitude of invariants within the rules in our ARS (As Dr.Kurz similarly mapped out on github):

Suppose we have this set of rules within our ARS:

a -> b <br/>
b -> a <br/>

From here, we can search for some invariants. Imagine these are lines of code that you are executing in order (from the top down). What isn't changing after we go through these rules? What /*patterns*/ are similar between these two lines?

Here are some examples of invariants that can be found within these rules:
length <br/>
number of a's <br/>
number of b's <br/>
any equation involving number of a's, number of b's, or length (ex: length + num a's, num b's - num a's, etc) <br/>


As Dr. Kurz mentions, this can be further divided into groups. While this is important, I feel that it is already covered extensively in the lecture notes.Since the idea of this blog is to bring more comfortability with the idea of invariants, I do not want to repeat examples from class.

Another way I found learning about invariants to be really helpful is looking through code for invariants. Even though I had written code before in various computing classes and didn't know the term invariant, I searched for them all the time... especially when checking my logic in loops.

With this, I think it's helpful to apply the concept of an invariant in an ARS to searching for invariants in code.

This is a program I had written in Java that involved a simple while loop involving substrings. While this is a simple program, we can still decode where invariants lie:

public class WordLength{
  public static void main(String [] args){

    Scanner scan = new Scanner(System.in);

    //Variables
    String word;
    int n = 0;

    //Ask user to enter a word
    System.out.println("Please enter any word you like in the box.");
    word = scan.nextLine();

    //while loop prints each letter to its own line.
    while(n < word.length()){
       System.out.println(word.substring(n,n+1));
       n++;
    }
  }
}

A few invariants lie within this small snippet of code:
scan = new Scanner(System.in) <br/>
n > 0 <br/>
n < word.length but ONLY within the while suite

One invariant I think is interesting is n < word.length. While this condition is not a global invariant within our entire program, it is technically an invariant within our while loop suite. The commands inside the while loop suite are **only** executed when n < word.length(), making it a consistent condition that is true. 

I think this makes a good relation between general encapsulation and invariants. When going through code to determine invariants, I felt more comfortable with the topic, felt more comfortable determining invariants in ARS's, and overall realized the importance of being aware of invariants when writing general code.
