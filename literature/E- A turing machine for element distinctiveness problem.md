The problem could be a little trickier. 
The language is $E = \{ \#x_{1}\#x_{2}\#\dots\# x_{l} | \text{ each } x_{l}\in \{ 0,1 \}^{*} \text{ and } x_{i} \not = x_{j} \text{ for each } i \not = j\}$
Now the idea is: 
We'll use two pointers, one pointing to the start and next that will cover all the points one by one. In simple terms, we'll check $x_{1}$ with $x_{2}$ , and $x_{3}$ until we reach $x_{l}$. After that we'll move to $x_{2}$ and compare that to $x_{3}$ and so on. Once we finished we could say there is no symbol that are equal (to know if they are equal we do by the method of zigzagoning).
![[Turing machine example for element distinctiveness problem.png]]

At first I didn't catch it, so we'll have an example to make this:
Imagine the next input $w =$ #100#111#101
first, we place the mark on the first # symbol
so
1- #' 100 # 111 # 101
Now we place the second
2- #' 100 #' 111 # 101
So we compare $x_{1}$ with $x_{2}$. In effect they are not equal. We continue then.
3- #' 100 # 111 #' 101. In effect they are not equal, we continue.
Now we reach the final, so we put the leftmost mark # to the second
4- # 100 #' 111 #' 101
We do that until we got finished and see if all strings are not equal.
# References
[[C-TOC- ch 3.1 Turing machines]]
[[E- A turing machine for a language consisting B = w]]