
The language is :
$A = \{ p^{2^{n}} | n \geq 0 \}$
The high level form is :
M2 = “On input string w:
1. Sweep left to right across the tape, crossing off every other 0.
2. If in stage 1 the tape contained a single 0, accept .
3. If in stage 1 the tape contained more than a single 0 and the
number of 0s was odd, reject .
4. Return the head to the left-hand end of the tape.
5. Go to stage 1.”

Here, for examle the 000.
We first cross around the ceros, first cero, two cero, and tree cero. Now, the tape contains an odd number of ceros then reject.
But for example with  0000, 
1,2,3,4 cero, since it is even, we return to the head, so now it is x0x0, we do the same, 1,2. we have an even, therefore we do it again, 1, great we see 1, therefore it's a power of 2. 
A turing machine for this it's:
![[State diagram for Turing machine E1.png]]

SO, here we put the label $0\to \sqcup,R$ means, from state q1, we read 0 as the input in the head, and change it to $\sqcup$ and we move to the right. The same for the other. A shorthand it's $0\to R$, that means on input 0 moves to R, but change nothing.

An example of this machine it's:
![[example of the state diagram Turing machine E1.png]]
# Referencias
[[C-TOC- ch 3.1 Turing machines]]
[[D- Language that is Turing -decidable]]