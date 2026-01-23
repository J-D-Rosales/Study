Let's called the procedure
![[Build-Max-Heap Pseudocode.png]]

Now, let's derive this into the simplest form.
We know that Max-Heapify has a running time of $lg(n)$, then running $\frac{n}{2}$ times, it gives an upper bound of $O(nlg(n))$. Nonetheless, making better analysis, will bring us a lower quota. 
In order to do so, we need to state the next property:
![[F-Number of nodes in a heap#^d6a761]]
A detail intuition / prove is given:
[[Number of nodes in any given h height in a heap]]
Now, let's do some analysis.
We need to sum all the costs from the nodes at each height, that will be:
$$
\sum _{h =0} ^{\lfloor lgn \rfloor } (\text{Something})
$$
The *Something* it's going to be the cost of each node at the specific level h. Now, the Max-Heapify procedure, view with height will cost $O(h)$. Then any node at $h$ height will have at most $O(h)$ time. Since we now, the number of nodes at any height $h$. We could do the next:
$$
\sum_{h= 0}^{\lfloor lgn \rfloor } \left( \left\lceil  \frac{n}{2^{h+1}}  \right\rceil \cdot ch \right)
$$
Now, by property and some analysis we have $\left\lceil  \frac{n}{2^{h+1}}  \right\rceil \geq \frac{1}{2}$ for $0 \leq h \leq lgn$. think that the worst case is that $h = lgn$, we got $\frac{n}{2n}$ that is $\frac{1}{2}$ so it still accomplished. then $\lceil x \rceil \leq 2x$ for all $x\geq \frac{1}{2}$. Therefore $\lceil  n / 2^{h+1} \rceil \leq \frac{n}{2^{h}}$. then
$$
\begin{align}
\sum_{h = 0} ^{\lfloor lgn \rfloor } \left( \left\lceil   \frac{n}{2^{h+1}}  \right\rceil \cdot ch \right)  \\
 & \leq \sum ^{\lfloor lgn \rfloor }_{h = 0} \left( \frac{n}{2^{h}}  \cdot ch \right) \\
 & = cn\sum_{h =0}^{\lfloor lgn \rfloor } \frac{h}{2^{h}} \\
 & \leq cn \sum ^{\infty}_{h = 0} \frac{h}{2^{h}} \\
 & = cn \left( \frac{1/2}{(1-1 / 2)^{2}}  \right) = O(n)
\end{align}
$$


#examples 
## References
[[6.3 Building a Heap]]