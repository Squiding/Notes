# Computational Method: NP Problem

There are many ways of thinking about NP and NP-completeness. I'll start with a definition of NP, then will talk about NP-hardness, and finally NP-completeness.

---

At a high level, **P** and **NP** are classes of problems. A problem is in **P** if it is a yes-or-no question (a *decision problem*) and there is some algorithm that solves the problem in polynomial time. For example, the question of *"can you get from node u to node v in this graph?"* belongs to P because you can solve it with depth-first search. (Note that DFS itself is not in P, since DFS is an algorithm rather than a problem). Another example of a problem in P would be checking whether a sequence is in sorted order.

A problem is in **NP** if it is a decision problem where a correct answer can be verified in polynomial time. A classic NP problem is the **subset sum problem**: given a set of weights and a target value *k*, can you pick a subset that sums exactly to *k*? It may be hard to find such a subset, but easy to verify if someone gives you a correct one—just sum the weights and check if the total equals *k*.

The name **nondeterministic polynomial** comes from an alternate view: imagine a magical algorithm that can *guess* the correct answer in polynomial time. In our weights example, such an algorithm would guess the correct subset, check if it sums to *k*, and return the result. If it's always guaranteed to make the correct guess, then it behaves like a polynomial-time verifier.

One of the most important open questions in computer science is whether every problem in NP is also in P. That is, if we can verify answers efficiently, can we also *find* them efficiently? We know P is a subset of NP, but we don’t know if NP ⊆ P.

---

### NP-Complete Problems

Some problems in NP are also **NP-complete**, meaning they are at least as hard as every other problem in NP. If we can solve any NP-complete problem efficiently, then every NP problem can be solved efficiently.

Formally, a problem is NP-complete if:
1. It is in NP, and
2. Any NP problem can be **reduced** to it in polynomial time.

Examples:
- Subset sum
- Boolean satisfiability (SAT)
- Integer programming
- Traveling salesman (decision version)
- Graph coloring
- Solving arbitrary-size Sudoku or Minesweeper boards

---

### NP-Hard Problems

Some problems are **NP-hard**, meaning they are at least as hard as any problem in NP, but they aren’t necessarily in NP themselves (e.g., they might not be decision problems).

---

### Practical Advice

If you're faced with an NP-complete or NP-hard problem in practice, don't expect a perfect solution quickly. Often, exact solutions are computationally infeasible. You might:
- Use **heuristics**
- Find **approximation algorithms**
- Solve a relaxed version of the problem

---

> Note: Only problems can be classified as NP or NP-complete—not algorithms. For example, DFS is an algorithm to solve the reachability problem, which itself is in P.

---

Hope this helps!
