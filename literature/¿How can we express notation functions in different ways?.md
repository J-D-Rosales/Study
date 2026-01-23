<span style="color:yellow">IDEA:</span>
We have a variety of forms in which we can express the notation functions, however we need to be careful on what it represents. 
Example:
$$
\sum _{i = 1} ^{n} O(i)
$$

Let's remember this is not a sum, it is a single function of i. So, it's not the same as $O(1) + O(2) + O(3) + O(4) + \dots O(n)$, which does not have a clean interpretation. 

<span style="color:yellow">Evidencia:</span>
For example, solving the first it's going to be:
We pick a one specific question $f(i)$ such that $f(i) \leq c$ for some constant.
$$
\sum _{i = 1} ^{ n} f(i) \leq \sum_{i = 1} ^{n} (c \cdot i) = c \cdot \frac{n(n+1)}{2} = O(n^{2}) 
$$
In the second form, the expression relates on several functions. This is messy because there gonna be a lot of constants.

**Tags:**

**Referencias**:
[[3.1 Asymptotic notation]]
[[¿What it means the running time of an algorithm if it's in Omega notation?]]
[[Theorem 3.1 for theta notation]]
[[D- of Omega notation]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

