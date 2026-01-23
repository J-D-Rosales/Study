created: 2025-11-10
**source:** [[C-TOC-cp4 - decidability]]
**tags:** #book_chapter 
## Resumen 
# Decidable problems concerning regular langauges
Talking about regular languages, is talking automatons. 
[[Acceptance problem for a DFA that accepts a given string]]
[[Theorem  4.1 of decidable language DFA]]
In order to prove the theorem, we need to create a Turing machine, however, the proof is left in the book, but we left the idea.
[[Proof idea for Theorem 4.1 of decidable language DFA]]
It's good see the book for the complete proof that is describing in a well manner the model.
Now, the proof for NOn-deterministic model it's similar, but other way it's handled for better variety.
[[Theorem 4.2 of decidable langauge NFA]]
[[Proof idea for Theorem 4.2 of decidable language NFA]]
Now, since the power of NFA and regular expressions are the same. We can convert the Regular expresions into a NFA and we do the same as the others models. I don't think it's necessary the theorem for that. 

Now, let's do another kind of testing.
[[¿What is an emptiness testing?]]
Now, let's state a theorem:
[[Theorem 4.4 for decidable langauge]]
The proofs it's really similar. 
[[Proof for Theorem 4.4 for decidable langauge.png]]
Next theorem it's really interesting: We'll say that if teo DFA's recognizes the same languages then they are decidable.
[[Theorem 4.5 Determining whether two DFA's recognizes the same languages]]
[[Proof idea for Theorem 4.5 Determining whether two DFA's recognizes the same languages]]

# Decidable Problem Concerning Context-Free Languages
We first show the decidability for CFG langauges.
[[Theorem 4.7 Decidability for CFG languages]]
[[Proof idea for Theorem 4.7 Decidability for CFG languages]]

We can of course improve this algorithm a lot, however, it terms of understanding we left as it is, and we address optimization later.
[[Theorem 4.8 Emptiness testing problem for CFG]]
[[Proof idea for Theorem 4.8 testing problem for E_CFG]]

You might think you can prove a lot of theorems more, but see the next:
the E_QCfg is not decidable. It test whether two CFL could have the same language, the proof for this is in next chapters.

[[Theorem 4.9 context-free-language-decidability]]
[[Proof idea for Theorem 4.9 context-free-language-decidability]]

## Referencias a notas permanentes
