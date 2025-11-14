created: 2025-11-09
**source:** [[C-TOC-cp3 - C H U R C H ----T U R I N G THESIS]]
**tags:** #book_chapter 
## Resumen 
Distinct type of models in the turing machines are called just like that variants of Turing machines.
[[¿What's the difference between Turing machine and variants of turing machines?]]
[[¿D- of robustness in Theory of computation for tuirng machines]]

# Multitape turing machines
[[D- Formal definition for multitape Turing machine]]
With this we can say the next theorem. 
[[Theorem 3.13 Multitape machines and single tape Turin machines]]
The proof of the theorem is left in the book (it's not worthy to note it all p.177). Intuiton is left behind.
[[Intuition for the proof of Theorem 3.13 Multitape machines and single tape Turing]]

It can go next that a language is turing recognizable is some multitape turing machine recognizes it.
# Non - deterministic turing machines.

[[D- Formal definition for a Non-deterministic turing machine]]
We as well let the proof in the book, but give an idea on how to prove it. 
[[Theorem 3.16 Non-deterministic turing machine equivales]]
[[Intuition for the proof of Theorem 3.16 Non-deterministic turing machine equivalent]]
From this we can have a corollary:
A language is turing recognizable if and only if some non-deterministic Turing machines recognizes it.
[[¿What its a decider in a nondeterministic turing machine?]]
From this we can make the next corollary
>[!tip] Corollary 3.19
>A language is decidable if and only if some non-deterministic turing Machines decides it.
# Enumerators
[[D- of a enumerators in Turing machines]]
The proofs are left in the book. 
[[theorem 3.21 Enumerators and turing machines]]
the idea is to consturct a turing mahcine that compares on every string input on enumerator. And the other way of the proof is to compute for every string the $\sum ^{*}$ where we compute the run M for i steps on each input $s_{1},s_{2}\dots$ possibles in the alphabet , if any accepts we print the corresponding $s_{j}$-

# Equivalence with other models
In few words, the modifications made to this lead to the conclusion that all have the same power or robustness. Even when different tiny thigs change on each definition. Finally the class of algorithm that it describes are the same for all models. It means, that in computers all programs can perform the same class of algorithm. In doing so, there is profound implications for this phenomenom.




## Referencias a notas permanentes
