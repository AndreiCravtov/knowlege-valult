A proof is a sequence of steps that result in some statement being proven at the end. A proof must be rigorous and follow [[Mathematical Reasoning|mathematical reasoning]]. In order to do so, it must only contain the [[#Acceptable Steps|acceptable steps]].

# Acceptable Steps
The following enumerated steps are enough to prove any true statement in mathematics. 

***NOTE:***
- The statements 'if $P$ then $Q$' and '$P$ implies $Q$' are different.
	- The first is reserved for a proof that assumes $P$ then proves $Q$.
	- The second is the result of applying the step [[#Showing '$P implies Q$'|'Showing implies']].
- Many common constructions are not acceptable in proofs
	- 'It is easy to see' / 'Obviously' / 'Clearly': If it’s really easy, show it.
	- 'It has to be the case that': It either is true, or it is not; it doesn’t have to be anything.
	- '$\therefore$' this is often used to justify a step, but is not a logical symbol; use the word *therefore* instead.
	- Mathematical symbols ($\implies \Longleftarrow \iff \wedge \vee \neg \dots$) are shorthand. They should *only* be used in (well-formed, complete) formulas, not as replacement for words. They are **not** formulas to be manipulated.
- [[Mathematical Reasoning#Statements|Statements]] must be clearly separate prom the language of the proof, as they are effectively of a different language. A way to do this is to wrap all statements you make in quotes and brackets.
## Assumption
If $P$ is assumed to hold, then $P$ holds, under said assumption.
i.e. Assume $P$ holds, then by assumption $P$ is true.

It could be useful to label assumptions $A_1, A_2, \dots$ so that it is easier to keep track of them and invoke them in the proof. 
## Showing '$P \wedge Q$'
$\dots P$ holds $\dots Q$ holds. Since both $P$ and $Q$ are true, we have that ‘$P \wedge Q$’ holds.

## Using '$P \wedge Q$'
$\dots$ '$P \wedge Q$' hold. Then P is true.
*or*
$\dots$ '$P \wedge Q$' hold. Then Q is true.

## Showing '$P \vee Q$'
$\dots P$ holds. Since $P$ is true, we have that ‘$P \vee Q$’ holds.
*or*
$\dots Q$ holds. Since $Q$ is true, we have that ‘$P \vee Q$’ holds.

## Using '$P \vee Q$': Proof by Cases
$\dots$'$P \vee Q$' holds. Assume $P$, $\dots$ then $R$ holds. Now assume $Q$,$\dots$ then $R$ holds. Then $R$ is true.

## Showing '$P \implies Q$'
*When only assuming $P$*:
Assume $P \dots Q$ holds. Then '$P \implies Q$' holds.

*When assuming $R$, $P$*:
Assume $P,R \dots Q$ holds. Then assuming $R$, we have '$P \implies Q$'.
or
Assume $P,R \dots Q$ holds. Then assuming $P$, we have '$R \implies Q$'.

## Using '$P \implies Q$'
$\dots P$ holds. $\ \dots$ '$P \implies Q$' holds. Then $Q$ is true.

## Showing '$\neg P$'
*When only assuming $P$*:
Assume $P$ holds. $\ \dots$ we have a contradiction. Then '$\neg P$' is true.

*When assuming $P,Q,R$*:
Assume $P,Q,R$ holds. $\ \dots$ we have a contradiction. Then assuming $Q$ and $R$, we have '$\neg P$'.
*or*
Assume $P,Q,R$ holds. $\ \dots$ we have a contradiction. Then assuming $P$ and $R$, we have '$\neg Q$'.
*or*
Assume $P,Q,R$ holds. $\ \dots$ we have a contradiction. Then assuming $P$ and $Q$, we have '$\neg R$'.

## Proof by Contradiction
Assume that '$\neg P$' holds. $\ \dots$ we have a contradiction. Then $P$ is true.

*Notice that this is the same as the step [[#Showing '$ neg P$'|'Showing not']].*
***NOTE**: use this step sparingly it can lead to confusion. A [[Constructive Mathematics|direct]] proof is preferred since it is 'stronger'*

## Principle of Explosion
$\dots$ we have a contradiction. From contradiction anything follows. Therefore $P$.

## Law of Excluded Middle
*This step introduces a new true statement about any statement $P$.*
For the statement P, we have '$P \vee \neg P$'.
*Then using this new statement, we can apply the step [[#Using '$P vee Q$' Proof by Cases|'Using cases']].*

## Showing '$\forall x ( \ P(x) \ )$'
Let $o$ be an arbitrary object. $\ \dots$ so $P(o)$ holds. So '$\forall x ( \ P(x) \ )$' holds.

## Using '$\forall x ( \ P(x) \ )$'
$\dots$ '$\forall x ( \ P(x) \ )$' holds. Let $o$ be an arbitrary object for which it holds. So we have '$P(o)$'.

## Showing '$\exists x ( \ P(x) \ )$'
Let $o$ be a certain object. $\ \dots$ so $P(o)$ holds. So '$\exists x ( \ P(x) \ )$' holds.

## Using '$\exists x ( \ P(x) \ )$'
$\dots$ '$\exists x ( \ P(x) \ )$' holds. Let $o$ be the object for which it holds. So '$P(o)$' holds.
*Here the object $o$ can be anonymous or already know.*