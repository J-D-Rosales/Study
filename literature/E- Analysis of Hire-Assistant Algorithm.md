Recall the procedure:
![[HIre-Assistant Procedure.png]]

Here, we are not focused on the running time of the algorithm but in the cost that represents hire x number of candidates. 
Let the terms $ci,ch,n,m$ be the cost of interview, the cost of hire, the n candidates, and the $m$ candidates that were hired, respectively.
If we interview all of them that would be $ci\cdot n$ and the cost of hire would be $ch\cdot m$. Based on that we could say that the time would be $O(ci\cdot n + ch\cdot m)$.
## Worst case analysis
The worst case analysis is when when we hire all of them, because were given to us in increment level. Therefore the cost would be $O(ch\cdot m)$, since this term dominates the equation.
#examples 

For context: [[E- Procedure of Hire-Assistant]] and the problem [[E- The hiring problem - Intuition]]
Here we are not analyzing the running time, we are analyzing how often a procedure updates it's notion of which element is currently winner. 
# Referencias
[[5.1 The hiring problem]]