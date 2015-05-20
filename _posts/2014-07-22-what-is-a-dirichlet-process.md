---
layout: post
title:  What is a Dirichlet Process?
---

### _A rambling, handwavy (and quite possibly incorrect) introduction._

I've been enjoying this [series of posts] [1] introducing Dirichlet Process
Mixture Models, but initially found them a little tough-going, in part because
I wasn't familiar with the Dirichlet Process, and couldn't find a gentle enough
introduction to the topic. As an attempt to remedy this, here are my notes on
reading through the [Wikipedia article] [2] on the topic and a couple of other
resources.

Wikipedia starts off by stating that a Dirichlet Process is a "probability
distribution over probability distributions". Let's write this down explicitly
A probability distribution, in very simplified terms [^1], is a function from
some set of events that we'll call <span>\\(E\\)</span> to the range \\([0,1]\\), subject to some additional constraints. With that in mind, we can represent the set of probability distributions over E with the definition:

\\[
  P : E \mapsto [0,1]
\\]


(If you're not familiar with the notation, think of this like a type signature.
In Haskell, this'd be something like `type P = E -> [0,1]`, abusing the notation
slightly to introduce a fictional type of numbers between zero and one.)

Now, this doesn't specify a specific probability distribution, but rather just
the general 'shape', or 'type' of all such probability distributions on
\\(E\\). For any non-empty [^2] set \\(E\\), there are many [^3] different
ways we can choose to assign the elements of \\(E\\) to the elements of \\([0,1]\\),
(while still satisfying the extra measure-theoretic constraints that we've
lazily swept under the carpet until we need them). In that case, since \\(P\\) is
a set like any other, we can use \\(P\\) as the set of events in a probability
distribution, giving a probability distribution over probability
distributions:

\\[
  PP : P \mapsto [0,1]
\\]

Or equivalently, substituting in our definition of \\(P\\):

\\[
  PP : \\{ E \mapsto [0,1] \\} \mapsto [0,1]
\\]

(This probably makes more sense in our Haskellish notation: `type POverP = (E ->
[0,1]) -> [0,1]`)

Now, families of probability distibutions (slightly less informally, subsets of
\\(P\\) above) can also be take _parameters_ which allow us to specify the exact
value of the distribution. These are (normally) numbers of some sort - integers,
reals, vectors or matrices, depending on the distribution. For simplicity, we'll
restrict our example to distributions with a single parameter that we'll call
\\(\theta\\) ("_theta_") [^4].

Let's update our definition of P to include the parameter:

\\[
  P^\prime_\theta : E \mapsto [0,1]
\\]

In our pseudo haskell notation, we might wrie this as type `P' = Parameter ->
E -> [0,1]`. Despite this not being proper Haskell code, I actually find this
characterisation to be quite useful. To see why, note that is we partially apply
a function of type `P'` to its first argument, we get back a function of type
`P`. The parameter acts as a sort of _index_ over the space of probability
distributions on `E`.

At this point, it's also helpful to define the concept of a _draw_ from
a probability distribution. A draw from \\(P\\) returns a random element of \\(E\\), where each \\( e \in E \\) has probability \\(P(e)\\) of being drawn.


When we have a distribution over other distributions though, (such as \\(PP\\)),
taking a draw from the distribution gives us back another distribution! We can
then take a draw from _that_ distribution, in order to get back an event. We
could imagine this is another distribution (call it \\(PP'\\)) over \\(E\\) which we derive
from \\(PP\\), and is parameterised by \\(P\\).


\\[
  PP^\prime_P : E \mapsto [0,1]
\\]

<!---  START HERE TIM. FIXME - the dirichlet process is like PP not PP',
although we're interested in creating a PP' thing like it. Introduce the concept
of parametirised families of distributions first! --->

The Dirichlet Process is one such distribution. It actually has two parameters,
the underlying distribution \\(P\\) (as in \\(PP^\prime\\) above), and the
'concentration parameter' \\(\alpha\\) (_"alpha"_), which is a postive real
number, and whose role we will discuss further in due course:

\\[
  \alpha \in \mathbb{R}^+ \\\\
  P : E \mapsto [0, 1] \\\\
  DP_{P,\alpha} : E \mapsto [0, 1]
\\]

[^1]: I'll gloss over the precise measure-theoretic details for the time being and bring them in when they become necessary.
[^2]: Remember those extra constraints we mentioned earlier? this is one of them.
[^3]: Uncountably many!
[^4]: Look at me, pretending to be a proper mathematician!

[1]: http://blog.datumbox.com/overview-of-cluster-analysis-and-dirichlet-process-mixture-models/
[2]: http://en.wikipedia.org/wiki/Dirichlet_process

