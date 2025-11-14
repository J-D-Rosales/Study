<span style="color:yellow">IDEA:</span>
The idea is as follows. 
We can simulate any Non-deterministic Turing machine by seeing it's configuration. LIke a tree, where the nodes are the configurations of a turing machine. Therefore, when a desired configuration is reached, then we can say it accepts the language. We must, however, make a breadth first search and not a depth first search, that's because if we do a depth first search we could make an infinitive path, and therefore, we could not reach all nodes. Therefore what we must do is visiting all nodes level by level ensuring that every node will be visited.

Some cuestions:
the branch of the tree is a branch of the non-determinism, and the root it's the initial configuration.


<span style="color:yellow">Evidencia:</span>


**Tags:**

**Referencias**: [[C-TOC- ch 3.2 Variants of Turing Machines]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Theorem 3.16 Non-deterministic turing machine equivales]]
[[D- Formal definition for a Non-deterministic turing machine]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
NO deterministic turing machine equivalent

<span style="color:	#87CEEB">South: What does this lead to</span>
Real proof on non deterministic turing machine.
