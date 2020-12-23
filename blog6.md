# ARS Exercise
## Blog 6

Consider the rewrite rules

> ab -> cc

> ac -> bb

> bc -> aa

plus rules saying that the order of letters does not matter. Starting from 15 `a`, 14 `b` and 13 `c`, is it possible to reach a configuration in which there are only `a`s or only `b`s or only `c`s?

> aaaaaaaaaaaaaaabbbbbbbbbbbbbbccccccccccccc - 15 `a`s, 14 `b`s, 13 `c`s


To make it easier to read, I decided to split into pairs.

> aa aa aa aa aa aa aa bb bb bb bb bb bb bb cc cc cc cc cc cc ac

> ac-> bb

> aa aa aa aa aa aa aa bb bb bb bb bb bb bb cc cc cc cc cc cc bb

I then rearranged them into pairs that match the given rules.

> ab ab ab ab ab ab ab ab ab ab ab ab ab ab cc cc cc cc cc cc bb

> ab->cc

> cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc bb

From here, the only rule that could be applied would be bc->aa

> bc bc -> aa aa

Then the ac->bb rule

> ac ac ac ac-> bb bb bb bb

Then back to the bc->aa rule

> bc bc bc bc bc bc bc bc->aa aa aa aa aa aa aa aa

Following this looping pattern, I would then be able to make this:

> bb bb bb bb bb bb bb bb bb bb bb bb bb bb bb bb cc cc cc cc cc
> bc bc bc bc bc bc bc bc bc bc bb bb bb bb bb bb bb bb bb bb bb
> aa aa aa aa aa aa aa aa aa aa bb bb bb bb bb bb bb bb bb bb bb
> ab ab ab ab ab ab ab ab ab ab ab ab ab ab ab ab ab ab ab ab bb

Now I can use the ab->cc rule, but upon doing this:

> cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc cc bb

I realize I am back where I stared. Even if I went a different route, it would all loop around. So this means that this reduction does not terminate. And it cannot reduce to only `a`s or only `b`s or only `c`s. This can be proven with an invariant.

Because of the way the rules are structured, you need a pair ab, bc, or ac to make a reduction. Alsp, given that the order of letters doesn't matter, the function only terminates if it can reduce to only letters of one type. So if I want to reduce the other two letters so that there is only one letter remaining, I need the same number of the other two letters.

For example:

> aaabbbcccc
> abababccc
> ccccccccc

Notice that I have an equal number of a and b, so I am able to reduce to only `c`s.

So an invariant could be (Number of `a`s == Number of `b`s)

This can also work for reducing to only `a`s or only `b`s.

(Number of `a`s == Number of `c`s) would reduce to only `b`s.

(Number of `b`s == Number of `c`s) would reduce to only `a`s.
