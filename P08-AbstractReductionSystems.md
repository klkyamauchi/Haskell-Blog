# Entry #8: Abstract Reduction Systems

Abstract Reduction Systems (ARS) were by far my favorite part of this class. While the reductions can be tedious, I find them pretty enjoyable nonetheless. When learning and solving problems with Abstract Reduction Systems, it reminded me a lot of learning about Deterministic Finite Automata (DFAs) in a 'Models of Computation' course I had previously taken. In a DFA, an input is taken in and will go through various states and will either be accepted or rejected. Much like this, an ARS will take an input and will be reduced to different forms and put into an equivalence class based on given rules. This post will help introduce you to Abstract Reduction Systems. 

#### What is an ARS? 
Abstract Reduction Systems are systems that help us abstract from the syntax of programs. They help us rewrite a set of elements or reduce them given some relation to be applied to them. 

By **formal definition**, an ARS is a set, A, together with a relation → ⊆ $A × A$. This system is denoted as ($A$,→).

#### Key Definitions and Concepts
For the following concepts, I will give the formal definition presented to me by my own professor as well as my own understanding of the term where needed. If you would like to view his page directly, I have linked it [here](https://hackmd.io/@alexhkurz/BJfvFVK8v). 

For the following terms, let $A$ be a set with relation → to form an ARS ($A$, →). In addition let the elements $a, b \in A$. 

**Reducible:** $a$ is said to be ***reducible*** if there is a $b$ such that $a → b$. In other words, if $a$ can be further rewritten or reduced given the relation, then it is ***reducible***. 
  
**Normal Form:** $a$ has a ***normal form*** $b$ if $a$ reduces to $b$ and $b$ is a normal form. We have reached a normal form if an element $a$ cannot be any further reduced given the rules of the relation.

**Joinable:** $a$ and $b$ are ***joinable*** if they reduce to the same element. This relationship is denoted as $a$ ↓ $b$. If two different sequences (elements of the set $A$) are able to reduce to the same sequence given the relation, then they are considered joinable. 

**Confluent:** a system is ***confluent*** if whenever an element $a$ reduces to $b$ and $c$, the elements $b$ and $c$ are **joinable**. We often referenced this as the "diamond rule" where we start with a sequence $a$ which can be reduced to both $b$ and $c$, which then respectively both reduce to the same sequence, say $d$ creating a diamond. 

**Terminating:** a system is said to be ***terminating*** if there does not exist an infinite sequence. A tip that a system is ***non-terminating*** is if there are two (or more) rules in a relation that create a infinite cycle, meaning they reduce to each other. For example, if $a → b$ is a reduction in the same system as $b → a$, you could go back and fourth between these rules infinitely and the system would be **non-terminating**. 


#### Working through an ARS

Given the scheme of rules:
BA → AB 
AB → BA
AA → B
BB → A
AB →
AAA → 

I will find the normal form of the sequence: AABABA
1. AABABA
2. BBABA
3. AABA
4. BBA
5. AA
6. B
   
To find the normal form "B", I went through the sequence step by step substituting the reductions given by the rules. After looking at the reduction and the system, does it terminate? While we were able to find a normal form for this sequence, this does not guarantee that the system terminates for every input. We know this system actually **does not** terminate since there is a set of rules (BA → AB and AB → BA) that would create an infinite computation. 
