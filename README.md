# Python Typing Council

## About the Typing Council

The Typing Council was created in [PEP 729](https://peps.python.org/pep-0729/) to
govern the Python type system. Its mandate is to ensure that the type system is
useful, usable, and stable.

The current members of the Council are:

* Eric Traut ([@erictraut](https://github.com/erictraut))
* Carl Meyer ([@carljm](https://github.com/carljm))
* Jelle Zijlstra ([@JelleZijlstra](https://github.com/JelleZijlstra))
* Rebecca Chen ([@rchen152](https://github.com/rchen152))
* Shantanu Jain ([@hauntsaninja](https://github.com/hauntsaninja))

## Decisions

The Council makes decisions in response to issues opened on this repo. Such
decisions include:

* Substantive changes to the specification for the type system
* Recommendations on [PEPs that relate to typing](https://peps.python.org/topic/typing/)

Any such issues should first be discussed on [discuss.python.org](https://discuss.python.org/c/typing/32)
before being submitted for a decision.

Before the Council makes a decision, the community should get a chance
to weigh in. The procedure for requesting a specification change
without a PEP is:

1. Post on [discuss.python.org](https://discuss.python.org/c/typing/32)
   about the topic
1. Once the decision has run its course, create a concrete proposal (i.e.,
   a proposed change to the spec) and make a pull request on the
   [python/typing](https://github.com/python/typing) repo.
1. Create an issue on this repo asking the Typing Council for a decision.
1. After at least a week, the Council will make a decision, which may be
   to accept the change, reject it, or modify it.

The following items will be helpful when proposing a change to the
specification:

* A survey of the current behavior of major type checkers
* A rationale for why the proposed behavior is better than alternatives
* An implementation or proposed implementation of the proposed behavior
  in at least one major type checker

## Purpose of this repo

This repo exists only as a place to record the Typing Council's
procedures and to ask for decisions from the Council. No substantive
discussions should take place on this repo.

## Decision-making considerations

The Council is new and we will need time to figure out what works best.
However, to help contributors, we are listing some factors we expect
to consider when making decisions.

* What do type checkers currently do? Proposed spec changes should
  come with a survey of current type checker behavior. If all type
  checkers currently behave one way, but the spec says something else,
  we should almost certainly change the spec.
* Are type checkers willing to implement the proposed behavior? Often,
  there will be some disagreement among type checkers. If type checker
  maintainers aren't able or willing to change their tool’s behavior,
  we may not be ready for a change.
* Is the proposed behavior well-specified? Much of the current spec is
  vague. We should gradually work to improve that, and in particular
  new spec changes should be clear and unambiguous.
* Does the proposed change make the type system more consistent?
  If so, we are more likely to accept it.
* Is the proposed change sound (in the type-theoretic sense)? The
  Python type system is known to be not fully sound, and there are
  differing opinions on whether and to what extent we should aim to
  make it sound, but in general, a change that brings us closer to
  soundness is better.
* What are the backward compatibility implications of the change?
  We believe that it is important to keep the type system stable
  and avoid gratuitous compatibility breaks.
* What would be the effect of the change on real-world code
  checked by type checkers? Does it result in more false positives
  or false negatives?
* Does the proposed change make the type system better for our
  users?
