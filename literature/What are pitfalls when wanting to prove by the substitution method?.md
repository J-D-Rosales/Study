<span style="color:yellow">IDEA:</span>
The most important pitfall is not proving the inductive step exactly and covering with asymptotic notation, that is mathematically inadmissible. 

<span style="color:yellow">Evidencia:</span>
Let's say you what to prove [[E- Subtleties when proving a guess in substitution method]] the example there and you say $T(n) \leq cn$. 
$$
\begin{align}
T(n)  & \leq 2(c \lfloor n / 2 \rfloor ) + n \\
 & \leq cn + n  \\
 & = O(n)
\end{align}
$$
that's wrong, because you prove for $cn +n$, not for $cn$. And you tried to hide that with asymptotic notation, which is worse. We need to prove the exact form. As you see if $T(n) \leq cn +n$ does not imply that $T(n) \leq cn$.

**Tags:**

**Referencias**:
[[4.3 The substitution method for solving recurrences]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

