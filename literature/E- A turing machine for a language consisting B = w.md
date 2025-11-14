The example for this turing machine is $B = \{ w \# w, w\in \{ 0,1 \}^{*} \}$-
In order to do this we state the alphabets for both:
$Q = \{ q_{1},\dots,q_{8},q_{accept},q_{reject} \}$.
$\sum = \{ 0,1, \# \}$ and $\Gamma = \{ 0,1,\#,x,  \sqcup\}$
The graph for the oslution is left below:
![[State diagram for Turing machine with lagnauge B- E2.png]]

Here we could state the next. The idea is that when it read 1 or 0, it goes to the right, and the state q3 or q2, will pass whatever 0 or 1 (that's what it means 0,1) util it reaches de # symbol, where we cross al the marked symbol and finally read the same input as before. Once we did that, we move through left, whatever symbol was, until we reach the #, on q6. in q7, we came accros until reach an $x$,and therefore everything continues the same in a loop.


# References
[[C-TOC- ch 3.1 Turing machines]]
[[D- Turing recognizable language]]