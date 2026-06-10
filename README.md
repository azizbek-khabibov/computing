# Theory of computation

## Language and strings.

A *language* is set of strings. Such as : `{hi, hello, 123, *&%^%&}`

`hi` is in the language for the example above, and `bye` is not.

.

`Union` of two languages gives a new language that contains all strings from both without repetition : `C = A U B`. 

Ex: `A = {a, b}, B = {b, c}, C = {a, b, c}`

.

`Intersection` of two languages gives a new language that contains all strings that are present both in `A` and `B` : `C = A ∩ B`. 

Ex: `A = {a, b}, B = {b, c}, C = {b}`

.

`Concatenation` of two languages gives a new language that contains combination of all strings in `A` and `B` : `C = A ○ B`.

Ex: `A = {a, b}, B = {b, c}, C = {ab, ac, bb, bc}`

.

`A ○ B` is different from `B ○ A` :

`A ○ B = {ab, ac, bb, bc}, B ○ A = {ba, bb, ca, cb}`

P.S. It is not about the order strings appear in the set, but the order they are combined, i.e. `ac` is different from `ca`.
