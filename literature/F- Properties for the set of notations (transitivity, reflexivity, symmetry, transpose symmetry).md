# Transitivity.
$$
\begin{align}
f(n)  & = \Theta(g(n))\text{ and } g(n) = \Theta(h(n)) \text{ imply } f(n) = \Theta(h(n)) \\
f(n)  & = O(g(n)) \text{ and } g(n) = O(h(n)) \text{ imply } f(n) = \Theta(h(n)) \\
f(n)  & = \Omega(g(n)) \text{ and } g(n) = \Omega(h(n)) \text{ imply } f(n) = \Theta(h(n)) \\
f(n)  & = o(g(n)) \text{ and } g(n) = o(h(n)) \text{ imply } f(n) = \Theta(h(n)) \\
f(n)  & = \omega(g(n)) \text{ and } g(n) = \omega(h(n)) \text{ imply } f(n)  = \Theta(h(n)) 
\end{align}
$$
# Reflexivity
$$
\begin{align}
f(n) = \Theta(f(n)) \\
f(n) = O(f(n)) \\
f(n) = \Omega (f(n))
\end{align}
$$
# Symmetry
$$
f(n) = \Theta (g(n)) \iff g(n) = \Theta(f(n))
$$
# Transpose Symmetry
$$
\begin{align}
f(n)  & = O(g(n)) \iff g(n) = \Omega(f(n)), \\
f(n)  &  = o(g(n)) \iff g(n) = \omega (f(n))
\end{align}
$$
How can we memorize this?
Easy: Just think this as real number a and b.
Therefore, 
$f(n) \in \Theta(g(n))$ means $a = b$
$f(n) \in O(g(n))$ means $a \leq b$
$f(n) \in \Omega(g(n))$ means $a \geq b$
$f(n) \in o(g(n))$ means $a < b$
$f(n) \in \omega(g(n))$ means $a> b$


The only one that does not hol is trhicotomy, it menas that a and b can be just a < b or a = b or a > b, there is not other option, but for notation this property does not hold. 

#formulas


#  References
[[3.1 Asymptotic notation]]