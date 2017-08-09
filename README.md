# L-system

This project presents the theory behind L-systems and their applications, and explores a Python implementation of L-systems.

L-system is a parallel system that relies on rewriting grammars, and is often used to generate biological fractals. The formal construction of L-systems includes the following components, as defined by Prusinkiewicz and Lindenmayer in their book “The Algorithmic Beauty of Plants”:: 

1. A set of variables: symbols that can be replaced by production rules
2. A set of constants: symbols that do not get replaced.
3. A single axiom which is a string composed of some number of variables and/or constants. The axiom is the initial state of the system and is notated by “ω”.
4. A set of production rules defining the way variables can be replaced with combinations of constants and other variables. A production consists of two strings - the predecessor (consisting of a single symbol) and the successor.

The rewriting pattern is the most significant feature of the L-systems. When it is rewritten at a higher order, every instance of the letter p will be replaced by the string s. Variations are allowed in the rules, although p must be a single character, and cannot be one of the special symbols =, +, -, !, |, [, ], <, >, @, /, \, _, c, or the space character. Rewriting is case-sensitive, so, x = xXx is different from x = xxx.

For example, here is Lindenmayer’s original L-system for modeling the growth of algae:

axiom: A
rules: (A->AB), (B->A)
On iteration n, the following strings are produced:
n = 0: A
n = 1: AB
n = 2: ABA
n = 3: ABAAB
n = 4: ABAABABA
...

And so on. The difference between L-system and a formal grammar is that in every iteration, we apply all the rules possible, while in the latter, only one rule is applied in every iteration.
   
