# Abstract Reduction Systems
## Blog 5

Let me start by giving a formal definition of an Abstract Reduction System (ARS).

**ARS**: a set `A` together with relation -> ⊆ A x A. Let (A, ->) be an ARS, A is a set, -> is a subset of Cartesian product of A x A.

This can look like a lot of gibberish to a beginner, I know it did to me. So it helps to break down each aspect of the definition.

**a set A**: a set can be defined in many ways, but commonly is seen to be a set of words or strings that can be produced by a group of letters or symbols. For example, a set A could be all the strings over {x, y, z, &, +}. This means that strings such as xxxyy, &+&xy, and yz++ could all be part of set A.

**relation -> ⊆ A x A**: -> is a relation that is used to show reduction in an abstract reduction system. -> is a subset, or Cartesian product of A x A. This represents all the possible combinations of symbols that are contained in A. It can also be said that a ∈ A, or a is an element of A. This will come in handy later when talking about reduction and normal forms.

Given further exploration into the first two parts of the definition, the rest starts to make sense.

**(A, ->)**: an ARS can be written as such, as A is the set, and -> is the relation on that set.

But what does this mean for an actual reduction system?

An ARS has a set of rules that allows for reduction. These rules define how to compute normal forms.

**A Normal Form** can also be defined by looking at its parts. Given an ARS (A, ->) and a ∈ A, if there exists no b such that (a, b) ∈ -> or that a->b, then a is the normal form.

So if we look at the relation a->b, we can say a reduces to b. This is true when there is a possible reduction given a set of rewrite rules. The easiest way to understand this is to look at an example.

Using the set as defined above, where A is the set of all strings over  {x, y, z, &, +}, the rules are as follows:

> yx -> xy

> z+& -> &z

> && ->

From here, we can compute the normal form of *yx&z+&* as follows:

>yx&z+& -> xy&z+& using the yx -> xy rule

>xy&z+& -> xy&&z using the z+& -> &z rule

>xy&&z -> xyz using the && ->   rule

*xyz* is the normal form, because there exists no b such that a -> b. Or rather, there are no further reductions that can be made from the given set of rules.
