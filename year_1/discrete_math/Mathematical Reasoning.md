Mathematical reasoning is a form of reasoning where very precise steps are followed to reach a conclusion that some statement holds. The result is often called a [[Formal Proofs|proof]] for that statement.

# Statements
Mathematical statements can be abstracted as letters such as $P$ or $Q$.

## Types of statements
Predicates are statements which have placeholders for objects: $P(x)$ or $Q(x)$. Saying '$P$ holds for $o$' is equivalent to $P(o)$.

'$P \wedge Q$' holds when both P and Q hold

| $P$ | $Q$ | $P \wedge Q$ |
| --- | --- | ------------ |
| F   | F   | F            |
| F   | T   | F            |
| T   | F   | F            |
| T   | T   | T            |

'$P \vee Q$' holds when either P or Q holds

| $P$ | $Q$ | $P \wedge Q$ |
| --- | --- | ------------ |
| F   | F   | F            |
| F   | T   | T            |
| T   | F   | T            |
| T   | T   | T            |

'$\neg P$' holds when P doesn't hold

| $P$ | $\neg P$ |
| --- | -------- |
| F   | T        |
| T   | F        |

'$P \implies Q$' holds when, if P holds, Q also holds

| $P$ | $Q$ | $P \implies Q$ |
| --- | --- | -------------- |
| F   | F   | T              |
| F   | T   | T              |
| T   | F   | F              |
| T   | T   | T              |

'$\forall x ( \ P(x) \ )$' holds when, $P$ holds for all objects
'$\exists x ( \ P(x) \ )$' holds when, $P$ holds for at least one object

## Operator precedence
When dealing with an ambiguous statement such as $\neg P \implies Q$, the unary operator has higher precedence than the binary operator, and should be read as $(\neg P) \implies Q$.
