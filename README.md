Problem

You are given a list of words sorted lexicographically according to an alien language.
Return a valid ordering of characters in that language.
If no valid ordering exists, return "".


---

Example

Input: ["wrt","wrf","er","ett","rftt"]
Output: "wertf"


---

🔹 Intuition

This is a graph + topological sort problem.

Steps:

1. Build a graph:

Compare adjacent words.

First differing character gives an ordering rule c1 → c2.

If prefix conflict (e.g. ["abc", "ab"]) → invalid.



2. Perform topological sort:

Use Kahn’s Algorithm (BFS) or DFS.

If cycle detected → return "".


# Alien-Dictionary-in-Java
