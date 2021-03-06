# Reasoning and Logic
FAQ For Reasoning and Logic
## Table of contents
1. [Disjunctive Normal Form](disjunctive-normal-form)
2. [De Morgan's Law](de-morgans-law)



## Disjunctive Normal Form
Disjunctive Normal Form or DNF for short is the disjunction of conjunctions of literals. Every formula has an equivalent in DNF.

### Examples of DNF
```
A 
	
A ∨ ¬A
	
A ∨ (B ∧ ¬C) ∨ D
```	

### Transformation Algorithm
There are several different methods for transforming an arbitrary formula into DNF. The following is one of the simplest with three steps:

1. Eliminate the connectives for implication (⇒) and equivalence (⇔) by rewriting using the following equivalences:
    * A ⇒ B is equivalent to ¬A ∨ B
    * A ⇔ B is equivalent to (¬A ∨ B) ∧ (A ∨ ¬B)
2. Push negations (¬) inside subformulas as far as possible, applying [De Morgan's Law](de-morgans-law) where possible, and eliminate double negations. We also handle the negation of the propositional constants. We do this by rewriting with the following equivalences: 
    * ¬(¬A) is equivalent to A
    * ¬(A ∧ B) is equivalent to ¬A ∨ ¬B
    * ¬(A ∨ B) is equivalent to ¬A ∧ ¬B
    * ¬t is equivalent to f
    * ¬f is equivalent to t
3. Distribute conjunctions (∧) over disjunctions (∨). We rewrite all applicable subterms of the formula using one of the following two equivalences:
    * A ∧ (B ∨ C) is equivalent to (A ∧ B) ∨ (A ∧ C)
    * (A ∨ B) ∧ C is equivalent to (A ∧ C) ∨ (B ∧ C)

## De Morgan's law
De Morgan's law states the following equivalences:
*   ¬(A ∧ B) ⇔ ¬A ∨ ¬B
*   ¬(A ∨ B) ⇔ ¬A ∧ ¬B


## Sources
* [DNF](http://www.barrywatson.se/cl/cl_dnf.html)
