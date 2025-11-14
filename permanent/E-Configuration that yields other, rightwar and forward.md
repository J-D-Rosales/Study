Let's say that we have $a,b,c \in \Gamma$, and the strings $u,v \in \Gamma^{*}$ and states $q_{i}$ and $q_{j}$. In that case $uaq_{i}bv$ and $uq_{j}ac v$ are two configurations. Say that:
$$
uaq_{i}bv \text{ yields } u q_{j}acv
$$
Now, it is true for $\delta(q_{i},b) = (q_{j},c,L)$. It means, from the state $q_{i}$ go to $q_{j}$, and b are going to be replaced by c, after that move to the left. Remember that the letter that is pointing is the next of the state.
Now for the right-forward.
$$
uaq_{i}bv \text{ yields } uacq_{j}v
$$
If, $\delta (q_{i},b) = (q_{j},c,R)$.
# References
[[C-TOC- ch 3.1 Turing machines]]
[[How a configuration in a turing machine yields another?]]
[[D- of a configuration of a turing machine]]
