<span style="color:yellow">IDEA:</span>
Given a sample space S and an event A, we can define a indicator random variable $I\{ A \}$ of A as:
$$
I\{ A \} = \begin{cases}
1 & \text{if A occurs}, \\
0  &  \text{if A does not occur}
\end{cases}
$$
An indicator random variable help us to convert into numeric the outputs of event.

<span style="color:yellow">Evidencia:</span>
Indicator random variable provides a convenient method for converting between probabilities and expectations. 
Let's put a sample space of flipping a fair coin. That is $S =\{ H,T \}$. Then, we define an indicator random variable $X_{H}$ related with the event H. This counts the number of heads obtain in this flip, 1 if it's Head and 0 if it's not.
$$
X_{H} = I_{H} = \begin{cases}
1  & \text{if H occurs} \\
0 &  \text{if T occurs}
\end{cases}
$$

To know the expected number of heads obtain in this flip. It's just the expected value of our indicator variable, $X_{H} =I_{H}$.
$$
\begin{align}
E[X_{H}] = E[I_{H}] = 1\cdot Pr\{ H \}  + 0\cdot pr\{ T  \} = \frac{1}{2} 
\end{align}
$$

**Tags:**
#definiton 
**Referencias**:
[[5.2 Indicator random variables]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
