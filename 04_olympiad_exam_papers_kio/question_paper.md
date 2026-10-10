# Kenya Informatics Olympiad (KIO) 2026
## First Round - Selection Exam

**Time Allowed:** 2 hours (120 minutes)  
**Total Marks:** 28 marks  
**Structure:**
- **Section A**: 12 multiple-choice questions (1 mark each).
- **Section B**: 8 multiple-choice questions (2 marks each).

---

### Instructions to Candidates
1. This paper contains **20 multiple-choice questions**.
2. Select the **single best option (A, B, C, D, or E)** for each question and record your answer on your answer sheet.
3. No calculators, phones, or programming devices are permitted.
4. Scratch paper is provided for rough work.
5. There is **no negative marking** for incorrect answers.

---

## Section A: Basic Computational Thinking (12 Questions, 1 Mark Each)

### Question 1 (Grid Paths with Obstacle)
A delivery robot navigates a grid of streets. The grid contains 4 horizontal streets and 4 vertical streets, forming intersections from $(0,0)$ at the bottom-left to $(3,3)$ at the top-right. 

The robot starts at $(0,0)$ and wants to reach $(3,3)$ by moving only East (right) or North (up). However, the intersection at $(2,1)$ is under construction, and the robot cannot pass through it. How many different valid routes can the robot take?
- **A.** 9
- **B.** 11
- **C.** 14
- **D.** 20
- **E.** 24

---

### Question 2 (Logic Gates)
Consider the following boolean logic circuit with three inputs ($A, B, C$) and one output ($Y$):
- Input $A$ and Input $B$ are connected to an **AND** gate. *(An AND gate outputs $1$ only when both inputs are $1$; otherwise it outputs $0$.)*
- The output of the AND gate and Input $C$ are connected to an **XOR** gate. *(An XOR gate outputs $1$ when its two inputs are different — one $0$ and one $1$; it outputs $0$ when they are the same.)*
- The output of the XOR gate is then inverted by a **NOT** gate to produce the final output $Y$. *(A NOT gate outputs the opposite of its input.)*

What are the output values of $Y$ for the input combinations $(A,B,C) = (1,0,1)$ and $(A,B,C) = (1,1,1)$ respectively?
- **A.** 0 and 0
- **B.** 0 and 1
- **C.** 1 and 0
- **D.** 1 and 1
- **E.** The output is undefined for these inputs

---

### Question 3 (Binary Search)
You have an alphabetically sorted list containing exactly $1000$ unique student names. You want to check if a specific student's name is in this list using the binary search algorithm. In the absolute worst case, what is the maximum number of name comparisons you will need to make to determine if the name is in the list?
- **A.** 9
- **B.** 10
- **C.** 11
- **D.** 12
- **E.** 7

---

### Question 4 (Stack Permutations)
A stack is a data structure that operates on a Last-In, First-Out (LIFO) basis. You push the integers `1, 2, 3, 4` onto the stack in that exact order, but you may interleave pushes and pops in any way. For example, pushing `1`, pushing `2`, popping `2`, popping `1`, pushing `3`, popping `3`, pushing `4`, popping `4` yields the output sequence `2, 1, 3, 4`.

Which of the following output sequences **cannot** be generated using this stack?
- **A.** `1, 3, 4, 2`
- **B.** `4, 3, 2, 1`
- **C.** `3, 1, 2, 4`
- **D.** `2, 4, 3, 1`
- **E.** `3, 4, 2, 1`

---

### Question 5 (Tree Traversals)
A **binary tree** is a structure where each node has at most two children, called the *left child* and the *right child*. Three standard ways to list all nodes of a binary tree are defined as follows:
- **Preorder**: visit the current node, then recursively list the left subtree, then the right subtree.
- **Inorder**: recursively list the left subtree, then visit the current node, then the right subtree.
- **Postorder**: recursively list the left subtree, then the right subtree, then visit the current node.

The preorder traversal of a binary tree gives: `A, B, D, E, C, F`.  
The inorder traversal of the same tree gives: `D, B, E, A, F, C`.  

Which of the following is the **postorder** traversal of this tree?
- **A.** `D, E, B, F, C, A`
- **B.** `D, B, E, F, C, A`
- **C.** `D, E, B, C, F, A`
- **D.** `E, D, B, F, C, A`
- **E.** `E, D, B, C, F, A`

---

### Question 6 (Eulerian Paths)
An Eulerian path is a path in a graph that visits every edge exactly once. A graph can be drawn without lifting the pen from the paper and without retracing any edge if and only if it contains an Eulerian path.

Which of the following five graphs **does not** contain an Eulerian path?
- **A.** A graph with vertices $\{1, 2, 3, 4, 5\}$ and edges `(1,2), (2,3), (3,4), (4,5), (5,1)`.
- **B.** A graph with vertices $\{1, 2, 3, 4\}$ and edges `(1,2), (1,3), (1,4), (2,3), (2,4), (3,4)`.
- **C.** A graph with vertices $\{1, 2, 3, 4, 5\}$ and edges `(1,2), (2,3), (3,4), (4,1), (1,5), (5,3)`.
- **D.** A graph with vertices $\{1, 2, 3, 4\}$ and edges `(1,2), (2,3), (3,4), (4,1), (1,3)`.
- **E.** A graph with vertices $\{1, 2, 3, 4, 5\}$ and edges `(1,2), (2,3), (3,4), (4,5)`.

---

### Question 7 (Matatu Terminus)
At a busy matatu terminus in Nairobi, each matatu occupies a loading bay from its arrival time until its departure time. The terminus manager wants to find the minimum number of loading bays required so that no two matatus share a bay at the same time.

Suppose 5 matatus have the following arrival and departure times (in minutes past midnight):
- Matatu 1: $[10, 100]$
- Matatu 2: $[50, 120]$
- Matatu 3: $[90, 150]$
- Matatu 4: $[110, 200]$
- Matatu 5: $[140, 180]$

What is the minimum number of loading bays required?
- **A.** 2
- **B.** 3
- **C.** 4
- **D.** 5
- **E.** 6

---

### Question 8 (Katende's Network)
Katende's local computer network has 5 computers, numbered 1 to 5. The connections between the computers are:
- Computer 1 is connected to: Computer 2, Computer 3, and Computer 4.
- Computer 2 is connected to: Computer 3.
- Computer 4 is connected to: Computer 5.

All connections are bidirectional. Wesonga is at Computer 1 and wants to send a message to Mutua at Computer 5. What is the minimum number of computers on a valid route from Computer 1 to Computer 5 (inclusive of both start and end computers)?
- **A.** 2
- **B.** 3
- **C.** 4
- **D.** 5
- **E.** 6

---

### Question 9 (Chessboard Bishops)
What is the maximum number of bishops that can be placed on a standard $8 \times 8$ chessboard such that no two bishops can capture each other? (Bishops attack along diagonals).
- **A.** 8
- **B.** 12
- **C.** 14
- **D.** 16
- **E.** 18

---

### Question 10 (Chessboard Knights)
What is the maximum number of knights that can be placed on a standard $8 \times 8$ chessboard such that no two knights can capture each other? (Knights attack in an "L-shape": two squares vertically and one square horizontally, or vice versa).
- **A.** 16
- **B.** 32
- **C.** 64
- **D.** 28
- **E.** 40

---

### Question 11 (Greedy Coin Change)
A country uses coin denominations of $1, 3,$ and $4$ shillings. The greedy algorithm for making change for a value $V$ repeatedly chooses the largest coin denomination that is less than or equal to the remaining amount.

What is the smallest value of $V$ for which the greedy algorithm uses **strictly more** coins than the optimal (minimum) number of coins?
- **A.** 5 shillings
- **B.** 6 shillings
- **C.** 7 shillings
- **D.** 8 shillings
- **E.** 9 shillings

---

### Question 12 (Counting Distributions)
You want to distribute 9 identical balls into 9 distinguishable bins, allowing any number of balls (including zero) in any bin. How many distinct ways can you distribute these balls?
- **A.** 24,310
- **B.** 48,620
- **C.** 19,600
- **D.** 11,440
- **E.** 15,625

---

## Section B: Advanced Computational Thinking (8 Questions, 2 Marks Each)

### Question 13 (Mountain Path)
A hiker in the Aberdare Ranges is given a triangular grid of numbers. The hiker starts at the top and at each step may move only to one of the two adjacent numbers in the next row down. The goal is to choose a path that maximizes the total sum of the numbers visited.

Given the following triangle:
```
    5
   9 6
  4 3 7
 2 8 1 9
```
What is the maximum possible path sum from the top to the bottom of this triangle?
- **A.** 22
- **B.** 24
- **C.** 26
- **D.** 27
- **E.** 29

---

### Question 14 (Cycle Chasing)
A **directed graph** is a set of nodes connected by one-way arrows (edges), each carrying a numerical weight. A **cycle** is a path that starts and ends at the same node without revisiting any other node. The **total weight** of a cycle is the sum of the weights of its edges.

A directed graph has 4 nodes (numbered 1 to 4) and 7 directed edges:
- Node 1 $\to$ Node 2 (weight $+2$)
- Node 2 $\to$ Node 3 (weight $-1$)
- Node 3 $\to$ Node 1 (weight $+2$)
- Node 1 $\to$ Node 4 (weight $+1$)
- Node 4 $\to$ Node 2 (weight $-3$)
- Node 4 $\to$ Node 3 (weight $+1$)
- Node 3 $\to$ Node 4 (weight $+5$)

Which of the following is a cycle with a **negative** total weight?
- **A.** Node 1 $\to$ Node 2 $\to$ Node 3 $\to$ Node 1
- **B.** Node 2 $\to$ Node 3 $\to$ Node 4 $\to$ Node 2
- **C.** Node 1 $\to$ Node 4 $\to$ Node 2 $\to$ Node 3 $\to$ Node 1
- **D.** Node 1 $\to$ Node 4 $\to$ Node 3 $\to$ Node 1
- **E.** No cycle in this graph has a negative total weight.

---

### Question 15 (Sweets and Ages)
Alice and Bob are each holding some integer number of sweets. 
- Alice says to Bob: *"If we each added the number of sweets we are holding to our (positive integer) age, my answer would be double yours. If we took the product of each person's sweets and age, my answer would be four times yours."*
- Bob replies: *"Why don't you give me 5 of your sweets, because then both our sum (of sweets and age) and product (of sweets and age) would be equal."*

What is the product of Alice and Bob’s ages?
- **A.** 30
- **B.** 40
- **C.** 50
- **D.** 60
- **E.** 75

---

### Question 16 (Nim Subtraction Game)
Alice and Bob play a subtraction game with a heap of 30 stones. In each turn, a player may remove exactly 1, 3, or 4 stones from the heap. The player who takes the last stone (leaving 0 stones) wins the game.

Both players play **optimally**: each player always makes the move that guarantees their own win if a winning strategy exists, or otherwise forces the game to be as difficult as possible for their opponent.

If Alice goes first, who has a winning strategy, and what is the winning first move if they have one?
- **A.** Alice has a winning strategy by removing 1 stone.
- **B.** Alice has a winning strategy by removing 3 stones.
- **C.** Alice has a winning strategy by removing 4 stones.
- **D.** Bob has a winning strategy (no first move by Alice can guarantee a win).
- **E.** The game is a draw under optimal play.

---

### Question 17 (The Ten Glasses)
Ten glasses stand in a row. Glass $i$ has a capacity of exactly $i$ litres, for $i=1, 2, \dots, 10$. Together, the glasses contain exactly $10$ litres of water, and each glass contains a whole number of litres.

In one move, you choose a source glass and a different destination glass, and pour from the source into the destination. You must continue pouring until either the source is empty or the destination is full. No water is spilled. 

Let $M_A, M_B, M_C$ be the minimum number of moves needed to leave exactly $1$ litre of water in every glass from starting configurations A, B, and C respectively:
- **A**: `[0, 2, 1, 1, 1, 1, 1, 1, 1, 1]` (Glass 2 contains 2L, Glass 1 contains 0L, others 1L)
- **B**: `[0, 0, 0, 0, 5, 1, 1, 1, 1, 1]` (Glass 5 contains 5L, Glasses 1-4 contain 0L, others 1L)
- **C**: `[0, 0, 0, 0, 0, 0, 0, 0, 0, 10]` (Glass 10 contains 10L, others 0L)

What is the value of the sum $M_A + M_B + M_C$?
- **A.** 10
- **B.** 12
- **C.** 14
- **D.** 15
- **E.** 18

---

### Question 18 (Chessboard Knights with 2 Attacks)
What is the greatest number of knights that can be placed on a $5 \times 5$ chessboard such that each knight attacks exactly 2 of the other placed knights?
- **A.** 12
- **B.** 14
- **C.** 16
- **D.** 18
- **E.** 20

---

### Question 19 (Join the Dots)
For each of the five point sets A, B, C, D, and E below, we want to connect all points using straight lines to form a *simple polygon* (a single closed cycle of edges that do not cross each other, using every point exactly once as a vertex). 

Let $P_A, P_B, P_C, P_D, P_E$ be the number of different simple polygons that can be formed from each respective set:
- **Set A (5 points)**: $(0,0), (4,0), (6,3), (3,6), (-1,4)$
- **Set B (4 points)**: $(0,0), (5,0), (1,4), (2,1)$
- **Set C (6 points)**: $(0,0), (5,0), (6,4), (2,6), (-1,3), (2,2)$
- **Set D (7 points)**: $(0,0), (6,0), (7,4), (4,7), (0,6), (-2,3), (2,2)$
- **Set E (7 points)**: $(0,0), (6,0), (7,5), (3,8), (-2,5), (2,2), (4,3)$

No three points in any set are collinear. What is the value of the sum $P_A + P_B + P_C + P_D + P_E$?
- **A.** 28
- **B.** 31
- **C.** 34
- **D.** 37
- **E.** 40

---

### Question 20 (The Hidden Set)
Exactly five of the ten numbers in $\{1, 2, \dots, 10\}$ are "bad". You want to identify which five numbers are bad. You can ask queries of the form: "Does subset $Q$ contain at least one bad number?". 

What is the minimum number of queries needed in the worst case to determine the exact set of bad numbers?
- **A.** 8
- **B.** 9
- **C.** 10
- **D.** 12
- **E.** 14

---
## End of Paper. Good Luck!
