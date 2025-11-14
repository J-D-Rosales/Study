The langauge is $C = \{a^{i}b^{j}c^{k} | i \times j = k\text{ and } i,j,k \geq 1\}$
![[State machine with words for the langauge for multiplication in turing machines.png]]

We can do this machine in several ways, however the idea is to have the a cross symbol and the b cross symbol. We need to take care of what is done in the come back. Some strategy to know if we are at the leftmost is to add a special character, and when you move to the left the special caracter is still there (because we have assumed that moving to the left when it's blank leaves to the same spot) SO if the caracter is the same we are at the leftmost spot.

# Refernces
[[C-TOC- ch 3.1 Turing machines]]
[[E- A turing machine for a language consisting B = w]]