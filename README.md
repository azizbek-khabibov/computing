# Theory of computation

## Language and strings.

A **language** is set of strings. Such as : `{hi, hello, 123, *&%^%&}`

`hi` is in the language for the example above, and `bye` is not.

.

**Union** of two languages gives a new language that contains all strings from both without repetition : `C = A U B`. 

Ex: `A = {a, b}, B = {b, c}, C = {a, b, c}`

.

**Intersection** of two languages gives a new language that contains all strings that are present both in `A` and `B` : `C = A ∩ B`. 

Ex: `A = {a, b}, B = {b, c}, C = {b}`

.

**Concatenation** of two languages gives a new language that contains combination of all strings in `A` and `B` : `C = A ○ B`.

Ex: `A = {a, b}, B = {b, c}, C = {ab, ac, bb, bc}`

.

`A ○ B` is different from `B ○ A` :

`A ○ B = {ab, ac, bb, bc}, B ○ A = {ba, bb, ca, cb}`

P.S. It is not about the order strings appear in the set, but the order they are combined, i.e. `ac` is different from `ca`.

.

`A*` gives the set of all possible combinations of the strings in `A`, which is infinite:

Ex: `A = {a, b}, A* = {ꜫ, a, b, aa, ab, bba, bbab, ...}`

P.S. Note that `A*` includes `ꜫ`, which represents empty string.

.

## Automata

Autoama is pluar of Automaton, which is essentially a machine that consists of multiple states and transits from one state to other depending on the input provided.

Ex: `input = aab, FA = {(A => a -> B , _ -> A), (B => a -> B, b -> End, _ -> A), (End => a -> B, _ -> A)}`

The above example is an Automaton which checks if a string ends with `ab`. The condition is True only if **FA** ends in `End` state. Note that for the definition above of `End`, if there is any input left, it exits the final state and jumps to A or B depending on the input.

This is **Deterministic Finite Automata**, or **DFA**, as the transition for any input for the current state is deterministic. 

For any **FA**, we define a tuple **M** : `M = (Q, W, d, q0, F)`, where:
- Q is the set of all states;
- W is the alphabet the FA uses;
- d is the transition function;
- q0 is the start state;
- and F is the set of final states.

A language is called **Regular language** if it is recognized by some FA.

