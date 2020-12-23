# Abstract Reduction System Relations
## Blog 8

When learning about Abstract Reduction Systems, I struggled to understand the different types of relations.
When talking about relations, it is said that

> R ⊆ A x A

Which means R (the relation) is a subset of the Cartesian Product A x A. So when we say

> a R b

it means that a is related to, or has a relation with b.

The 3 types of relations that I want to talk about are reflexive, symmetric, and transitive closure.

### Reflexive

Reflexive was definitely hard for me to grasp. The relation can be written as

> x R x

I tried to think of it as a relation where both sides are equivalent, but that definition didn't fit quite right. It helped me to think of it as what happens when you take a step. For a reflexive relation, you can take zero steps. Relations such as `=` , `<=` and `>=` are reflexive because x is equal to x, x is less than or equal to x, and x is greater than or equal to x.

### Symmetric

The next relation I tried to figure out was symmetric. A Symmetric relation can be written as

> x R y => y R x

Which seems similar to the reflexive relationship, which is what I believe got me stuck. But in this case, the best way to figure out if a relationship is symmetric is to invert it. For example, if x < y is true, then is y < x also true? If so, then the relationship is symmetric. But given that x and y are different values, this x < y and y < x should never be true, because the only case where that is true is when both values are equal, and therefore the relationship is reflexive. So instead, I think of a non mathematical relationship as a example.

Let's say that Jane and Tommy both work in an office. Jane's relation to Tommy is that Tommy is Jane's coworker. Could you say that Tommy's relation to Jane is also coworker? Yes, so the relation is symmetric. If we said that Tommy was Jane's boss, then the relaionship wouldn't be symmetric, because Jane can't be Tommy's boss if Tommy is her boss.

### Transitive

The last relationship is transitive. I think transitive was easier for me to understand, because I recognize the root of the word. Trans means across, so a transitive relation is one that continues across multiple relations. This can be written as

> x R y & y R z => x R z

Using `<` and `>` works better here. If x < y is true and y < z is true, then x < z is true, so `<` is a transitive relation. This also works for `>`.

Thinking of each of these relationships as a number of steps, I would sum these relationships as

> Reflexive- I can take 0 steps

> Symmetric- I can change direction

> Transitive- I can take as many steps as I want
