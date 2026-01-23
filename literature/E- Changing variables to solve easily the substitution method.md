<span style="color:yellow">IDEA:</span>
Having a Recurrence that seems difficult but it resembles to some you have seen so far, you can change variables and see if it is similar to the recurrences you have seen and therefore, do it quickly.

<span style="color:yellow">Evidencia:</span>
Let's put $T(n) = 2T(\lfloor \sqrt{ n } \rfloor) + \log_{2} n$
It seems really weirs, however, changing the variables being $m = \log_{2} n$. And, for convenience (for this example) not worry about rounding the values we have:
$T(2^{m}) = 2 T(2^{m/2}) + m$
Now, taking a new recurrence $S(m) = T(2^{m})$.
$$
S(m) = 2S(m /2) + m
$$
And of course you know this; the answer is  $m\log m$. So changing everything.
$$
T(n) = T(2^{m}) = S(m) = O(m\log m) = O(\log_{2}n \log_{2}(\log_{2}n))
$$

**Tags:**

**Referencias**:
[[4.3 The substitution method for solving recurrences]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[What are pitfalls when wanting to prove by the substitution method?]]
[[E- Subtleties when proving a guess in substitution method]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

