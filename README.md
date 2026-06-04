# Formula Key for `probability_theory_extension_of_logic.ipynb`

This README is a companion guide for the notebook. It explains the notation, symbols, and formulas used in the argument that probability theory is **partly** an extension of logic, but not identical to classical logic or First-Order Logic.

## Core idea

The notebook compares two mathematical systems:

- **Classical logic:** statements are either true or false.
- **Probability theory:** statements/events receive numerical weights between impossible and certain.

The central distinction is:

$$
\text{truth} \neq \text{probability}
$$

Read as: “Truth is not the same mathematical object as probability.”

---

## Symbol key

| Symbol | How to read it | Meaning |
|---|---|---|
| $A,B,C$ | “proposition A, B, C” | Statements or events being reasoned about |
| $v(A)$ | “the truth value of A” | A logical valuation assigning true or false |
| $P(A)$ | “the probability of A” | A probability assigned to event/proposition $A$ |
| $P(A \mid B)$ | “probability of A given B” | Conditional probability |
| $\{0,1\}$ | “the set zero one” | The two classical truth values |
| $[0,1]$ | “the interval from zero to one” | The range of probability values |
| $\in$ | “is an element of” | Membership in a set |
| $\lor$ | “or” | Logical disjunction |
| $\land$ | “and” | Logical conjunction |
| $\neg A$ | “not A” | Negation of $A$ |
| $\leftrightarrow$ | “if and only if” | Logical equivalence |
| $\Rightarrow$ | “implies” | Logical implication or consequence |
| $\not\Rightarrow$ | “does not imply” | The implication fails |
| $\equiv$ | “is equivalent to” | Equivalence or identity of meaning |
| $\not\equiv$ | “is not equivalent to” | Not the same concept |
| $\bot$ | “bottom” or “contradiction” | A logically impossible statement |
| $\forall x$ | “for all x” | Universal quantifier |
| $\models$ | “semantically entails” | Logical consequence |
| $\Gamma,\Delta$ | “Gamma, Delta” | Sets of premises or assumptions |
| $\cup$ | “union” | Combining two sets |
| $D$ | “domain D” | The set of objects in a First-Order Logic structure |
| $X$ | “random variable X” | A variable whose value is assigned probabilistically |
| $f$ | “function f” | A proposed mathematical function |

---

# Formula guide

## 1. Classical logic uses truth values

### Truth-value assignment

$$
v(A) \in \{0,1\}
$$

Read as: “The truth value of $A$ is an element of the set $\{0,1\}$.”

Meaning: in classical logic, $A$ is either false or true.

---

### Truth and falsehood

$$
1 = \text{true}, \qquad 0 = \text{false}
$$

Read as: “One means true, and zero means false.”

Meaning: classical logic uses binary truth values.

---

### Law of excluded middle

$$
v(A \lor \neg A)=1
$$

Read as: “The truth value of $A$ or not-$A$ is true.”

Meaning: in classical logic, either $A$ is true or its negation is true.

---

### Law of non-contradiction

$$
v(A \land \neg A)=0
$$

Read as: “The truth value of $A$ and not-$A$ is false.”

Meaning: a statement and its negation cannot both be true.

---

## 2. Probability uses measures

### Probability assignment

$$
P(A) \in [0,1]
$$

Read as: “The probability of $A$ is in the interval from zero to one.”

Meaning: probability assigns a real number between impossibility and certainty.

---

### Intermediate probability

$$
P(A)=0.5
$$

Read as: “The probability of $A$ is one half.”

Meaning: $A$ is neither assigned classical truth nor classical falsehood. It has partial probability.

---

### Logical range

$$
\{0,1\}
$$

Read as: “The set containing zero and one.”

Meaning: the range of classical truth values.

---

### Probabilistic range

$$
[0,1]
$$

Read as: “The closed interval from zero to one.”

Meaning: the range of probability values.

---

## 3. Logic as a special case of probability

### Binary-valued probability

$$
P(A) \in \{0,1\}
$$

Read as: “The probability of $A$ is either zero or one.”

Meaning: this is the special case where probability behaves like classical truth valuation.

---

### Probability of negation

$$
P(\neg A)=1-P(A)
$$

Read as: “The probability of not-$A$ equals one minus the probability of $A$.”

Meaning: the probabilities of a proposition and its negation add to one.

---

### If $A$ is certain

$$
P(A)=1
$$

then:

$$
P(\neg A)=0
$$

Read as: “If $A$ has probability one, then not-$A$ has probability zero.”

Meaning: certainty of $A$ forces zero probability for its negation.

---

### If $A$ is impossible

$$
P(A)=0
$$

then:

$$
P(\neg A)=1
$$

Read as: “If $A$ has probability zero, then not-$A$ has probability one.”

Meaning: impossibility of $A$ forces certainty of its negation.

---

### Non-binary probabilities

$$
P(A)=0.3, \qquad P(A)=0.5, \qquad P(A)=0.999
$$

Read as: “The probability of $A$ may be 0.3, 0.5, or 0.999.”

Meaning: probability allows values that are not classical truth values.

---

### Boolean truth values inside probability values

$$
\text{Boolean truth values } \{0,1\} \subset [0,1]
$$

Read as: “The Boolean truth values zero and one are a subset of the probability interval from zero to one.”

Meaning: classical binary logic can be embedded as an extreme case of probability.

---

## 4. Logical connectives versus probabilistic connectives

### Truth values determine disjunction

$$
v(A)=1, \qquad v(B)=0
$$

Read as: “$A$ is true, and $B$ is false.”

Then:

$$
v(A \lor B)=1
$$

Read as: “The truth value of $A$ or $B$ is true.”

Meaning: in classical logic, the truth of $A \lor B$ is determined by the truth values of $A$ and $B$.

---

### Probability of disjunction

$$
P(A \lor B)=P(A)+P(B)-P(A \land B)
$$

Read as: “The probability of $A$ or $B$ equals the probability of $A$ plus the probability of $B$ minus the probability of $A$ and $B$.”

Meaning: probability must subtract the overlap so the shared part is not double-counted.

---

### Overlap term

$$
P(A \land B)
$$

Read as: “The probability of $A$ and $B$.”

Meaning: the amount of overlap between $A$ and $B$.

---

## 5. Counterexample showing probability is not truth-functional

### Same marginal probabilities

$$
P(A)=0.5, \qquad P(B)=0.5
$$

Read as: “$A$ has probability one half, and $B$ has probability one half.”

Meaning: both cases in the counterexample start with the same individual probabilities.

---

### Case 1: mutually exclusive events

$$
P(A \land B)=0
$$

Read as: “The probability of both $A$ and $B$ is zero.”

Meaning: the events do not overlap.

Therefore:

$$
P(A \lor B)=0.5+0.5-0=1
$$

Read as: “The probability of $A$ or $B$ is one.”

Meaning: when two half-probability events do not overlap, their union covers the whole space.

---

### Case 2: overlapping events

$$
P(A \land B)=0.25
$$

Read as: “The probability of both $A$ and $B$ is 0.25.”

Meaning: the events overlap by one quarter.

Therefore:

$$
P(A \lor B)=0.5+0.5-0.25=0.75
$$

Read as: “The probability of $A$ or $B$ is 0.75.”

Meaning: because there is overlap, the union is less than one.

---

### Same inputs, different outputs

$$
P(A)=0.5, \qquad P(B)=0.5
$$

but:

$$
P(A \lor B)=1
$$

in one case, while:

$$
P(A \lor B)=0.75
$$

in the other.

Read as: “The same individual probabilities can produce different probabilities for $A$ or $B$.”

Meaning: $P(A \lor B)$ is not determined by $P(A)$ and $P(B)$ alone.

---

### Hypothetical truth-functional probability rule

$$
P(A \lor B)=f(P(A),P(B))
$$

Read as: “The probability of $A$ or $B$ is some function of only the probabilities of $A$ and $B$.”

Meaning: the notebook argues that no such universal function exists.

---

## 6. Probability one is not always logical necessity

### Continuous random variable example

$$
A = \{X \neq 1/2\}
$$

Read as: “$A$ is the event that $X$ is not equal to one half.”

Meaning: $A$ excludes exactly one point from the interval.

---

### Probability one event

$$
P(A)=1
$$

Read as: “The probability of $A$ is one.”

Meaning: $A$ happens almost surely in the continuous model.

---

### Probability zero point

$$
P(X=1/2)=0
$$

Read as: “The probability that $X$ equals one half is zero.”

Meaning: a single exact point has probability zero under a continuous uniform distribution.

---

### The point is still possible in the sample space

$$
X=1/2
$$

Read as: “$X$ equals one half.”

Meaning: this is still a mathematically possible value, even though it has probability zero.

---

### Probability one versus logical necessity

$$
P(A)=1
$$

does not mean:

$$
A \text{ is logically necessary}
$$

Read as: “Probability one does not automatically mean $A$ is logically necessary.”

Meaning: “almost sure” is not always the same as “logically unavoidable.”

---

### Probability zero versus logical impossibility

$$
P(A)=0
$$

does not always mean:

$$
A \text{ is logically impossible}
$$

Read as: “Probability zero does not automatically mean $A$ is logically impossible.”

Meaning: in continuous probability, possible events can have probability zero.

---

## 7. Logical equivalence and equal probability

### Logical equivalence

$$
A \leftrightarrow B
$$

Read as: “$A$ if and only if $B$.”

Meaning: $A$ and $B$ have the same truth value in every relevant case.

---

### Equivalent propositions have equal probability

$$
P(A)=P(B)
$$

Read as: “The probability of $A$ equals the probability of $B$.”

Meaning: if two propositions are logically equivalent, they must receive the same probability.

---

### Fair coin example

$$
P(\text{Heads})=0.5
$$

Read as: “The probability of heads is one half.”

and:

$$
P(\text{Tails})=0.5
$$

Read as: “The probability of tails is one half.”

So:

$$
P(\text{Heads})=P(\text{Tails})
$$

Read as: “Heads and tails have the same probability.”

Meaning: equal probability does not imply logical equivalence.

---

### Mutual exclusivity

$$
\text{Heads} \land \text{Tails} = \bot
$$

Read as: “Heads and tails together equal contradiction.”

Meaning: a single coin toss cannot be both heads and tails.

---

## 8. First-Order Logic formulas

### Universal statement

$$
\forall x \, P(x)
$$

Read as: “For every $x$, $P(x)$ holds.”

Meaning: every object in the domain satisfies predicate $P$.

Note: here $P(x)$ is a **predicate**, not a probability function. This is a notation collision with $P(A)$ for probability.

---

### Domain with two objects

$$
D=\{a,b\}
$$

Read as: “The domain $D$ contains $a$ and $b$.”

Meaning: the logical structure has two objects.

---

### Universal claim over the domain

$$
\forall x\, P(x)
$$

Read as: “For all $x$, $P(x)$ is true.”

Meaning: in the domain $\{a,b\}$, this requires both $P(a)$ and $P(b)$.

---

### Predicate truth conditions

$$
P(a) \text{ is true and } P(b) \text{ is true}
$$

Read as: “$P$ holds of $a$, and $P$ holds of $b$.”

Meaning: the universal statement is true exactly when both objects satisfy the predicate.

---

### Probability assigned to a predicate claim

$$
P(P(a))=0.7
$$

Read as: “The probability that predicate $P$ holds of $a$ is 0.7.”

Meaning: this adds probability on top of First-Order Logic.

Note: the outer $P(\cdot)$ means probability; the inner $P(a)$ is a predicate statement.

---

### Probability assigned to a universal claim

$$
P(\forall x\,P(x))=0.2
$$

Read as: “The probability that $P(x)$ holds for every $x$ is 0.2.”

Meaning: First-Order Logic alone does not assign this number; a probability measure must be added.

---

### Logic plus probability structure

$$
\text{Logic} + \text{measure/probability distribution}
$$

Read as: “Logic plus a measure or probability distribution.”

Meaning: probabilistic First-Order reasoning requires extra mathematical structure.

---

## 9. Logical consequence versus probabilistic updating

### Logical entailment

$$
\Gamma \models A
$$

Read as: “Gamma entails $A$.”

Meaning: the premises in $\Gamma$ logically guarantee $A$.

---

### Monotonicity of classical logic

$$
\Gamma \cup \Delta \models A
$$

Read as: “Gamma together with Delta still entails $A$.”

Meaning: adding more premises does not invalidate a classical logical consequence.

---

### Example of deductive consequence

$$
\text{All humans are mortal}, \quad \text{Socrates is human}
$$

therefore:

$$
\text{Socrates is mortal}
$$

Read as: “From all humans being mortal and Socrates being human, it follows that Socrates is mortal.”

Meaning: this is deterministic deductive inference.

---

### Probabilistic update with more information

$$
P(\text{flies} \mid \text{bird})=0.95
$$

Read as: “The probability that something flies, given that it is a bird, is 0.95.”

But:

$$
P(\text{flies} \mid \text{bird} \land \text{penguin})=0.01
$$

Read as: “The probability that something flies, given that it is a bird and a penguin, is 0.01.”

Meaning: adding information can dramatically change probabilities.

---

## 10. Compact disproof formulas

### Proposed universal disjunction function

$$
f:[0,1]^2 \to [0,1]
$$

Read as: “$f$ maps a pair of numbers in $[0,1]$ to a number in $[0,1]$.”

Meaning: this is the hypothetical function that would make probabilistic disjunction truth-functional.

---

### Proposed rule

$$
P(A \lor B)=f(P(A),P(B))
$$

Read as: “The probability of $A$ or $B$ is determined only by the probabilities of $A$ and $B$.”

Meaning: the notebook shows this cannot work.

---

### Case 1 contradiction requirement

$$
P(A)=0.5, \qquad P(B)=0.5, \qquad P(A \land B)=0
$$

Then:

$$
P(A \lor B)=0.5+0.5-0=1
$$

So:

$$
f(0.5,0.5)=1
$$

Read as: “For the same pair of inputs, the function would have to output one.”

---

### Case 2 contradiction requirement

$$
P(A)=0.5, \qquad P(B)=0.5, \qquad P(A \land B)=0.25
$$

Then:

$$
P(A \lor B)=0.5+0.5-0.25=0.75
$$

So:

$$
f(0.5,0.5)=0.75
$$

Read as: “For the same pair of inputs, the function would have to output 0.75.”

---

### Contradiction

$$
1 \neq 0.75
$$

Read as: “One is not equal to 0.75.”

Meaning: the same input cannot produce two different outputs, so no such universal function $f$ exists.

---

## 11. Final conclusion formulas

### Truth is not probability

$$
\text{truth} \neq \text{probability}
$$

Read as: “Truth is not equal to probability.”

Meaning: truth values and probability measures are different mathematical objects.

---

### Probability one is not logical necessity

$$
P(A)=1 \not\equiv A \text{ is logically necessary}
$$

Read as: “$P(A)=1$ is not equivalent to saying $A$ is logically necessary.”

Meaning: probability one does not always mean logical certainty.

---

### Probability zero is not logical impossibility

$$
P(A)=0 \not\equiv A \text{ is logically impossible}
$$

Read as: “$P(A)=0$ is not equivalent to saying $A$ is logically impossible.”

Meaning: probability zero does not always mean contradiction.

---

### Equal probability is not logical equivalence

$$
P(A)=P(B) \not\Rightarrow A \leftrightarrow B
$$

Read as: “Equal probabilities do not imply that $A$ and $B$ are logically equivalent.”

Meaning: two different propositions can have the same probability.

---

### Disjunction needs overlap information

$$
P(A \lor B) \text{ is not determined by } P(A),P(B) \text{ alone}
$$

Read as: “The probability of $A$ or $B$ cannot be calculated from only the separate probabilities of $A$ and $B$.”

Meaning: the overlap term $P(A \land B)$ is also needed.

---

# One-line takeaway

Probability theory can embed classical logic when probabilities are restricted to $0$ and $1$, but full probability theory uses additional measure-theoretic structure and does not preserve every feature of classical deductive logic.
