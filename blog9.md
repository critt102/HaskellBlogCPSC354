# Equivalence Classes and Invariants
## Blog 9

I find myself getting Invariants and Equivalence classes mixed up. By definition,

> Invariants are statements that capture properties of computations that don’t change

When it comes to Abstract Reduction systems, Invariants are used to describe Equivalence classes, which means that they are closely related.
I think this is why I always confused them.

An example of an Invariant is # of a's and an example of an Equivalence class is 3 a's. So you can see how I got confused.
One of the first times I started to really grasp the difference between these two was for when I was studying for the midterm exam. A question on the practice exam asked me to describe the Equivalence classes of an ARS using an invariant.
 
At this point, I already knew that [] was an Equivalence class, and that the invariant was (# of a's - # of b's) mod 3.
This is when things started to click.

If I want to use (# of a's - # of b's) mod 3, I need to figure out when that equation will produce a normal form of []. I determined that the case is when

> (# of a's - # of b's) mod 3 = 0

From there, I wrote this relation

> The Equivalence class of [] is the set of all words such that (# of a's - # of b's) mod 3 = 0

I realized that Equivalence classes are really defined by the normal forms, or lack there of, of an ARS. And that the invariants could be turned into equations that proved that these normal forms existed.
From here I had to make sure I didn't mix this up with Equivalence relations, which are:

> Equivalence relation- a relation that is reflexive, transitive and symmetric

So I thought of it in terms of a real world example.

Being a "family" is a Equivalence relation. The Equivalence classes are different families that are related internally, but are not related to each other. So they all fall under the ARS, but they are separated by their normal forms and invariants.
