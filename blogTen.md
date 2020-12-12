# Blog No. 10
## Hoare Logic: Pre and Post Conditions

As we neared the end of the course, I found that the subject matter of Hoare logic was really interesting, and as a software engineering major, I compared it to processes I learned in designing and testing software in my other classes.

This blog will briefly explain Hoare logic and the Hoare triple, while making a comparison to that of pre and post conditions in software testing in the hopes of maybe helping future software engineering majors get a better grasp of Hoare logic in this course!

### Hoare logic

**Hoare logic** is a formal system that provides a set of rules to determine and reason the correctness of computer programs. I almost think of it as a spell check, or going through an essay and proofreading a rough draft. The point of Hoare logic is to provide a specific and logical way to **prove the validity** of an algorithm.

An extremely significant part of Hoare logic is the **Hoare triple**. At first when reading over what the Hoare triple is, I was a bit confused because it seemed somewhat complicated. I'm hoping that this will help to somewhat simplify the concept:

#### The Hoare Triple

The **Hoare triple** describes how the execution of a piece of code is going to change the "state" of computation. In the Hoare triple, there consists three parts that follow this structure:

{P}C{Q} <br/>

P = pre condition <br/>
Q = post condition <br/>
C = our command <br/>

When our **pre condition** (P) is met, our **command** (C) executes and therefore brings about the **post condition** (Q).

With this structure of the Hoare triple, we can prove **partial completeness** and **termination** respectively. This is described quite well in the link that Dr. Kurz included in his lecture notes for Hoare logic:

  "the intuitive reading of a Hoare triple is: Whenever P holds of the state before the execution of C, then Q will hold afterwards, or C does not terminate. In the latter case, there is no "after", so Q can be any statement at all. Indeed, one can choose Q to be false to express that C does not terminate."

  Link to source:
  https://en.wikipedia.org/wiki/Hoare_logic

### Software Engineering Comparison

With knowing the basics of Hoare logic and the Hoare triple, I drew a large parallel to the Hoare triple to creating **test cases**. Creating test cases was one activity I became comfortable with when in SE 300, Software Testing and Requirements.

The purpose of a test case in software engineering is to ensure that various features within a system are performing as expected and to ensure that a system is satisfying necessary standards. Similar to the purpose of Hoare logic, test cases **verify the correctness of a software feature**.

The test case includes various parts:

Test case ID: simply identifies the test case in which we are addressing <br/>
Test case description: describes the specific function/ feature that is being laid out <br/>
**Pre condition**: what must happen before the steps of the function are executed <br/>
Test case option (1 or more): outlines one (or more) of the specific ways a function/feature can differ in steps of execution <br/>
**Step no/ step description**: simply defines different steps of the feature (i.e. "User will press login button", "User will enter username and password") <br/>
**Post condition**: describes the state of the application/ system after the feature has been used for its intended purpose

Here is an example of a test case I created for a software system like Canvas, where professors must create classes that are verified before students can join them:



The highlighted steps draw parallels between the Hoare triple and a software engineering test case. I thought this was extremely interesting because of how well the two logical processes align, despite one being used for theoretical computing or even coding of a program, while the other deals with ensuring a created application or product is working as intended. In addition, I think it revealed to me that Hoare logic is not as niche and solely connected to theoretical computing, but instead used very largely to ensure correctness through the cycle of creating software.
