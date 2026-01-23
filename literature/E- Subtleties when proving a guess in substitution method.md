<span style="color:yellow">IDEA:</span>
When you have to prove a inequality and it does not hold for a constant, you can make another guess subtracting the initial guess by a constant d, and therefore when you do your inductive hypothesis all holds perfectly.


<span style="color:yellow">Evidencia:</span>
Let's say you want to prove $T(n) = T(\lfloor n / 2 \rfloor) + T(\lceil n / 2 \rceil ) + 1 = O(n)$. Your guess is totally right, however when you try to prove it. 
$T(n) \leq c \lfloor  n  / 2 \rfloor + \lceil n / 2 \rceil + 1$
$= cn + 1$.
As you see, this does not imply $T(n) \leq cn$.
That's when we change our guess to be $T(n) \leq cn -d$ where d > 0 is a constant. We now have. 
$$
\begin{align}
T(n)  & \leq (c \lfloor n / 2 \rfloor -d ) + (c \lceil  n / 2 \rceil -d) +1 \\
 &  = cn - 2d + 1 \\
 & \leq cn -d
\end{align}
$$
Now, we just need to choose a large c to handle the boundary conditions. 

**Tags:** #examples 
**Referencias**:
[[4.3 The substitution method for solving recurrences]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[¿How can we make a good guess in choosing a function for the substitution method?]]
[[E- of using the substitution method to solve the recurrence T(n)= 2T(n 2) + n]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

