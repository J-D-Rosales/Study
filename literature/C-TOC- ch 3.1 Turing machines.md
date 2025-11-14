created: 2025-11-02
**source:** [[B-Introduction to theory of computation]]
**tags:** #book_chapter 
[[C-TOC-cp3 - C H U R C H ----T U R I N G THESIS]]
## Resumen 
The model of a turing machine is with no restriction of memory. It can do everything a computer can do. 
[[Intuition or schematic of a Turing machine]]
[[How turing machines are a better representation of languages in compute theory]]
Even though we can describe a turing machine, the details are in the formal definition which is as follows:
[[D-formal definition of a turing machine]]
The turing machine works towards a configuration
[[D- of a configuration of a turing machine]]

[[How a configuration in a turing machine yields another?]]
Special cases of configuration arise when the head is pointing at one of the ends of configuration.
[[Special cases of a Configuration in a Turing machine]]
For this book, when the head is pointing to black in the leftward way, we eliminate the blanck space and the head is gonna point to the first element that is not blanck, that case does not follow for the right part. 

¿What are the most important configuration?
[[¿What is a start configuration in a turing machine?]]
[[¿What is an accepting configuration in a turing machine?]]
[[¿What is a rejecting configuration in a turing machine?]]
[[¿What are halting configuration in a turing machine ?]]

A more complicated way to define the turing machine is if we take off the accpet state, and the reject state.

[[¿When a turing machine accepts an input w?]]
Now, when we know that A turing machine can recognize an input string w, we could say:
[[¿What is the lenguaje of a Turing machie?]]

Now we go to a definition:
[[D- Turing recognizable language]]

[[¿What is a loop in a Turing Machine?]]

Now we want to handle turing machine that accept inputs or reject inputs, therefore machines that halt. So, we called the deciders. 
A decider that recognize some language we said to decide that language. 
[[¿What it's decidability in Turing Machines?]]
[[D- Language that is Turing -decidable]]

REmeber that every decidable langauge is turing recognizable.
Normally we would decribe the turing mahcines with the states or formal definition, but are really large. Therefore, we'll do it in high level.
[[E- A turing machine for a language consisting of all ceros whose lenght is a power of 2]]
[[E- A turing machine for a language consisting B = w#w]]
[[E- A turing machine for a language consisting on multiplication]]
[[E- A turing machine for element distinctiveness problem]]
## Referencias a notas permanentes
